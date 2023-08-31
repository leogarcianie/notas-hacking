# Level 8 🡪 Level 9
## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit8
Password: TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
## Solución
```
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ wc data.txt
 1001  1001 33033 data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| sort | Ordenar las líneas de texto de un archivo. |
| uniq | Filtrar las líneas de texto únicas. |
| -u | Mostrar las líneas únicas. |
## Referencias
https://overthewire.org/wargames/bandit/bandit9.html