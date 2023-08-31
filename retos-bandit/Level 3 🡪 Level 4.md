# Level 3 🡪 Level 4
## Objetivo
The password for the next level is stored in a hidden file in the **inhere** directory.
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit3
Password: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
## Solución
```
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| la -a | Muestra los archivos ocultos. |
## Referencias
https://overthewire.org/wargames/bandit/bandit4.html