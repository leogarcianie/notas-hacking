# Level 27 🡪 Level 28
## Objetivo
There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo` via the port `2220`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit27
Password: YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
```
## Solución
```
bandit27@bandit:~$ mktemp -d
/tmp/tmp.rcE6lydsrN
bandit27@bandit:~$ cd /tmp/tmp.rcE6lydsrN
bandit27@bandit:/tmp/tmp.rcE6lydsrN$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit27/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit27/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit27-git@localhost's password:
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
bandit27@bandit:/tmp/tmp.rcE6lydsrN$ ls -la
total 10564
drwx------   3 bandit27 bandit27     4096 Sep 24 20:19 .
drwxrwx-wt 154 root     root     10801152 Sep 24 20:19 ..
drwxrwxr-x   3 bandit27 bandit27     4096 Sep 24 20:19 repo
bandit27@bandit:/tmp/tmp.rcE6lydsrN$ ls
repo
bandit27@bandit:/tmp/tmp.rcE6lydsrN$ cd repo/
bandit27@bandit:/tmp/tmp.rcE6lydsrN/repo$ ls
README
bandit27@bandit:/tmp/tmp.rcE6lydsrN/repo$ cat README
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR
bandit27@bandit:/tmp/tmp.rcE6lydsrN/repo$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| git clone | Clonar el repositorio indicando el link y el puerto. |
## Referencias
https://overthewire.org/wargames/bandit/bandit28.html