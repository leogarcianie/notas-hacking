# PW Crack 2
## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://artifacts.picoctf.net/c/13/level2.py          
--2023-10-01 02:07:41--  https://artifacts.picoctf.net/c/13/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.88, 18.154.132.32, 18.154.132.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.88|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: ‘level2.py’

level2.py                   100%[==========================================>]     914  --.-KB/s    in 0s      

2023-10-01 02:07:41 (10.7 MB/s) - ‘level2.py’ saved [914/914]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
--2023-10-01 02:07:50--  https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.88, 18.154.132.32, 18.154.132.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.88|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: ‘level2.flag.txt.enc’

level2.flag.txt.enc         100%[==========================================>]      31  --.-KB/s    in 0s      

2023-10-01 02:07:51 (9.19 MB/s) - ‘level2.flag.txt.enc’ saved [31/31]
   
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
level2.flag.txt.enc  level2.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ nano level2.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python           
Python 3.11.4 (main, Jun  7 2023, 10:13:09) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36))
de76
>>> exit()

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 level2.py
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 
```
## Notas adicionales
## Referencias