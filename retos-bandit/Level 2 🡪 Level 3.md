# Level 2 🡪 Level 3
## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit2
Password: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
## Solución
```
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| cat "archivo con espacios" | Muestra el contenido de un archivo de texto que tenga espacios en su nombre. |
## Referencias
https://overthewire.org/wargames/bandit/bandit3.html