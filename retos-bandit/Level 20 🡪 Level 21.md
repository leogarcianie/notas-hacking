# Level 20 🡪 Level 21
## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit20
Password: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
```
## Solución
```
bandit20@bandit:~$ nc -lnvp 2020 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 3970860
bandit20@bandit:~$ Listening on 0.0.0.0 2020

bandit20@bandit:~$ ./suconnect 2020
Connection received on 127.0.0.1 40882
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
bandit20@bandit:~$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| nc | Conectar puertos de un host. |
## Referencias
https://overthewire.org/wargames/bandit/bandit21.html