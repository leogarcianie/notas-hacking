# Level 19 🡪 Level 20
## Objetivo
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit19
Password: awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```
## Solución
```
bandit19@bandit:~$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Apr 23 18:04 .
drwxr-xr-x 70 root     root      4096 Apr 23 18:05 ..
-rwsr-x---  1 bandit20 bandit19 14876 Apr 23 18:04 bandit20-do
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit19@bandit:~$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| setuid | Permiten a los usuarios ejecutar un ejecutable con los permisos del sistema de archivos del propietario o grupo del ejecutable respectivamente y cambiar el comportamiento en los directorios. |
## Referencias
https://overthewire.org/wargames/bandit/bandit20.html
https://en.wikipedia.org/wiki/Setuid