# PW Crack 3
## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://artifacts.picoctf.net/c/17/level3.py          
--2023-10-01 02:13:09--  https://artifacts.picoctf.net/c/17/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.74, 18.154.132.32, 18.154.132.88, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: ‘level3.py’

level3.py                   100%[==========================================>]   1.31K  --.-KB/s    in 0s      

2023-10-01 02:13:10 (28.6 MB/s) - ‘level3.py’ saved [1337/1337]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
--2023-10-01 02:13:17--  https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.74, 18.154.132.32, 18.154.132.88, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: ‘level3.flag.txt.enc’

level3.flag.txt.enc         100%[==========================================>]      31  --.-KB/s    in 0s      

2023-10-01 02:13:18 (12.0 MB/s) - ‘level3.flag.txt.enc’ saved [31/31]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://artifacts.picoctf.net/c/17/level3.hash.bin    
--2023-10-01 02:13:29--  https://artifacts.picoctf.net/c/17/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.74, 18.154.132.32, 18.154.132.88, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: ‘level3.hash.bin’

level3.hash.bin             100%[==========================================>]      16  --.-KB/s    in 0s      

2023-10-01 02:13:29 (8.75 MB/s) - ‘level3.hash.bin’ saved [16/16]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
level3.flag.txt.enc  level3.hash.bin  level3.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ nano level3.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 level3.py
Please enter correct password for flag: f09e
That password is incorrect

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 level3.py
Please enter correct password for flag: 4dcf
That password is incorrect

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 level3.py
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 
```
## Notas adicionales
## Referencias