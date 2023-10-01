# fixme2.py
## Objetivo
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/5/fixme2.py)
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://artifacts.picoctf.net/c/5/fixme2.py                                           
--2023-10-01 01:48:31--  https://artifacts.picoctf.net/c/5/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.108, 18.154.132.74, 18.154.132.88, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.108|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: ‘fixme2.py’

fixme2.py                   100%[==========================================>]   1.00K  --.-KB/s    in 0s      

2023-10-01 01:48:32 (2.10 MB/s) - ‘fixme2.py’ saved [1029/1029]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
fixme2.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 fixme2.py
  File "/home/kali/Desktop/picoCTF/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ nano fixme2.py                         

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 
```
## Notas adicionales
## Referencias