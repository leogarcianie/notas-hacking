# Level 14 🡪 Level 15
## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit14
Password: fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```
## Solución
```
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

^C
bandit14@bandit:~$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| nc (netcat) | Nos permite conectarnos a un host de un puerto especifico. |
## Referencias
https://overthewire.org/wargames/bandit/bandit15.html
[IP Addresses](http://computer.howstuffworks.com/web-server5.htm)
[Localhost on Wikipedia](https://en.wikipedia.org/wiki/Localhost)
[Ports](http://computer.howstuffworks.com/web-server8.htm)