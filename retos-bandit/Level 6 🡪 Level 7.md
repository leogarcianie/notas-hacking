# Level 6 🡪 Level 7
## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit6
Password: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
## Solución
```
bandit6@bandit:~$ ls
bandit6@bandit:~$ ls /
bin   drifter     home     lib32   lost+found  opt   run   srv  usr
boot  etc         krypton  lib64   media       proc  sbin  sys  var
dev   formulaone  lib      libx32  mnt         root  snap  tmp
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| find / -user bandit7 -group bandit6 -size 33c 2>/dev/null | Se encuentra un archivo con find, del usuario bandit7, grupo bandit6 y tamaño 33c. Y los archivos que no se pudieron revisar son enviados como errores. |
## Referencias
https://overthewire.org/wargames/bandit/bandit7.html