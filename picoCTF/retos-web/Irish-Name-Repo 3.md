# Irish-Name-Repo 3
## Objetivo
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/40742/` ([link](https://jupiter.challenges.picoctf.org/problem/40742/)) or http://jupiter.challenges.picoctf.org:40742. Try to see if you can login as admin!
## Solución
```
Se utiliza un método de encriptación para el password de tipo rot-13, entonces después de desencriptar nuestro password ' or 1 == 1; ahora es ' be '1'='1, y se valida introduciendo la contraseña y ya de ahí se obtiene la flag.

# Logged in!
Your flag is: picoCTF{3v3n_m0r3_SQL_4424e7af}
```
## Notas adicionales
## Referencias