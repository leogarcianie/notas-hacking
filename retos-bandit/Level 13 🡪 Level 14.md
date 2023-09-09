# Level 13 🡪 Level 14
## Objetivo
The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit13
Password: wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
## Solución
```
bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p 2220
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

  Enjoy your stay!

bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:~$ exit
logout
Connection to localhost closed.
bandit13@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.

C:\Users\leoga>
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| ssh | Permite conectarse a un servidor remoto, en este caso lo utilizamos mediante una llave para conectarse al servidor del usuario bandit14 y de ahí obtener su llave privada para poder acceder al siguiente nivel. |
## Referencias
https://overthewire.org/wargames/bandit/bandit14.html