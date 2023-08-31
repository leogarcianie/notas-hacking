# Level 9 🡪 Level 10
## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit9
Password: EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
## Solución
```
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ file ./*
./data.txt: data
bandit9@bandit:~$ strings data.txt | grep ==
4========== the#
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| strings | Obtiene los caracteres de un archivo que es no legible. |
| grep | Busca las líneas de texto que contengan cierto carácter. |
## Referencias
https://overthewire.org/wargames/bandit/bandit10.html