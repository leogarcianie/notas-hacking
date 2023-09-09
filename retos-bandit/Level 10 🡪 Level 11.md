# Level 10 🡪 Level 11
## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit10
Password: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
## Solución
```
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| base64 | Codifica un mensaje de texto a base64. |
| base64 -d | Decodifica un mensaje que ya estaba codificado en base64. |
## Referencias
https://overthewire.org/wargames/bandit/bandit11.html