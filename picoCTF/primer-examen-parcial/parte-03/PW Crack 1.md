# PW Crack 1
## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://artifacts.picoctf.net/c/11/level1.py          
--2023-10-01 02:03:00--  https://artifacts.picoctf.net/c/11/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.108, 18.154.132.88, 18.154.132.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.108|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: ‘level1.py’

level1.py                   100%[==========================================>]     876  --.-KB/s    in 0s      

2023-10-01 02:03:01 (1.76 MB/s) - ‘level1.py’ saved [876/876]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
--2023-10-01 02:03:09--  https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.108, 18.154.132.88, 18.154.132.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.108|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: ‘level1.flag.txt.enc’

level1.flag.txt.enc         100%[==========================================>]      30  --.-KB/s    in 0s      

2023-10-01 02:03:09 (9.16 MB/s) - ‘level1.flag.txt.enc’ saved [30/30]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls    
level1.flag.txt.enc  level1.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat level1.flag.txt.enc
A
 Rr1w▒Q nVT_nPRVW▒                                                                                                               
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ nano level1.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 level1.py      
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 
```
## Notas adicionales
## Referencias