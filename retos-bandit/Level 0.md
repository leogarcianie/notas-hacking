# Level 0
## Objetivo
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is **bandit.labs.overthewire.org**, on port 2220. The username is **bandit0** and the password is **bandit0**. Once logged in, go to the [Level 1](https://overthewire.org/wargames/bandit/bandit1.html) page to find out how to beat Level 1.
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit0
Password: bandit0
```
## Solución
```
C:\Users\leoga>ssh bandit0@bandit.labs.overthewire.org -p 2220

bandit0@bandit.labs.overthewire.org's password:

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us on discord or IRC.

  Enjoy your stay!

bandit0@bandit:~$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| pwd | Me indica el directorio actual. |
| whoami | Saber el usuario actual. |
## Referencias
- [Secure Shell (SSH) on Wikipedia](https://en.wikipedia.org/wiki/Secure_Shell)
- [How to use SSH on wikiHow](https://www.wikihow.com/Use-SSH)