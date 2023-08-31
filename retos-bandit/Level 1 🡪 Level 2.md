# Level 1 🡪 Level 2
## Objetivo
The password for the next level is stored in a file called **-** located in the home directory
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit1
Password: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
## Solución
```
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| cat ./- | Muestra el contenido de un archivo de texto que comience con -. |
## Referencias
https://overthewire.org/wargames/bandit/bandit2.html