# Irish-Name-Repo 1
## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/50009/` ([link](https://jupiter.challenges.picoctf.org/problem/50009/)) or http://jupiter.challenges.picoctf.org:50009. Do you think you can log us in? Try to see if you can login!
## Solución
```
Se realiza una inyección sql por una vulnerabilidad, en este caso se utilizó ' or 1 == 1;, esto hace que se ignore la validación de la contraseña y ya de ahí se obtiene la flag.

# Logged in!
Your flag is: picoCTF{s0m3_SQL_fb3fe2ad}
```
## Notas adicionales
## Referencias