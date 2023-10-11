# Irish-Name-Repo 2
## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/53751/` ([link](https://jupiter.challenges.picoctf.org/problem/53751/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:53751
## Solución
```
Se realiza una inyección sql por una vulnerabilidad, en este caso se utilizó admin'; con esto se hace que no se haga valida la consulta y se valida sin introducir una contraseña y ya de ahí se obtiene la flag.

# Logged in!
Your flag is: picoCTF{m0R3_SQL_plz_c34df170}
```
## Notas adicionales
## Referencias