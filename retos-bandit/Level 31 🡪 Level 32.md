# Level 31 🡪 Level 32
## Objetivo
There is a git repository at `ssh://bandit31-git@localhost/home/bandit31-git/repo` via the port `2220`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit31
Password: OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
```
## Solución
```
bandit31@bandit:~$ mkdir /tmp/leo31
bandit31@bandit:~$ cd /tmp/leo31
bandit31@bandit:/tmp/leo31$ git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), done.
bandit31@bandit:/tmp/leo31$ cd repo
bandit31@bandit:/tmp/leo31/repo$ ls
README.md
bandit31@bandit:/tmp/leo31/repo$ cat README.md
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master

bandit31@bandit:/tmp/leo31/repo$ ls -a
.  ..  .git  .gitignore  README.md
bandit31@bandit:/tmp/leo31/repo$ rm .gitignore
bandit31@bandit:/tmp/leo31/repo$ nano key.txt
Unable to create directory /home/bandit31/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit31@bandit:/tmp/leo31/repo$ ls
key.txt  README.md
bandit31@bandit:/tmp/leo31/repo$ git add key.txt
bandit31@bandit:/tmp/leo31/repo$ ls -la
total 20
drwxrwxr-x 3 bandit31 bandit31 4096 Sep 29 01:27 .
drwxrwxr-x 3 bandit31 bandit31 4096 Sep 29 01:22 ..
drwxrwxr-x 8 bandit31 bandit31 4096 Sep 29 01:28 .git
-rw-rw-r-- 1 bandit31 bandit31   15 Sep 29 01:27 key.txt
-rw-rw-r-- 1 bandit31 bandit31  147 Sep 29 01:22 README.md
bandit31@bandit:/tmp/leo31/repo$ rm .gitignore
rm: cannot remove '.gitignore': No such file or directory
bandit31@bandit:/tmp/leo31/repo$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   key.txt

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    .gitignore

bandit31@bandit:/tmp/leo31/repo$ git commit -m "commit"
[master 5adc4d9] commit
 1 file changed, 1 insertion(+)
 create mode 100644 key.txt
bandit31@bandit:/tmp/leo31/repo$ git log
commit 5adc4d98102e8e8f8c7a75fd054f774f3a7dfb1a (HEAD -> master)
Author: bandit31 <bandit31@overthewire.org>
Date:   Fri Sep 29 01:29:24 2023 +0000

    commit

commit 362bfd50c2007554b4aac93af07ebf964179a7b7 (origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:43 2023 +0000

    initial commit
bandit31@bandit:/tmp/leo31/repo$ git push
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 315 bytes | 315.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'
bandit31@bandit:/tmp/leo31/repo$
```
## Notas adicionales
## Referencias