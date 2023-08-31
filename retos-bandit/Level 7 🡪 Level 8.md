# Level 7 🡪 Level 8
## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit7
Password: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
## Solución
```
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ man grep
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| grep | Comando para buscar una palabra en un archivo e imprimir lo que contiene. |
## Referencias
https://overthewire.org/wargames/bandit/bandit8.html