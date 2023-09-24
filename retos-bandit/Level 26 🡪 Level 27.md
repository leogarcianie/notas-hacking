# Level 26 🡪 Level 27
## Objetivo
Good job getting a shell! Now hurry and grab the password for bandit27!
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit26
Password: c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
```
## Solución
```
:set shell=/bin/bash

:shell

bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$ ./bandit27-do id
uid=11026(bandit26) gid=11026(bandit26) euid=11027(bandit27) groups=11026(bandit26)
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$
```

## Notas adicionales
## Referencias
https://overthewire.org/wargames/bandit/bandit27.html