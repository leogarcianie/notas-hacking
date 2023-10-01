# fixme1.py
## Objetivo
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://artifacts.picoctf.net/c/26/fixme1.py                                       
--2023-10-01 01:28:35--  https://artifacts.picoctf.net/c/26/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.74, 18.154.132.108, 18.154.132.32, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: ‘fixme1.py’

fixme1.py                   100%[==========================================>]     837  --.-KB/s    in 0s      

2023-10-01 01:28:35 (8.25 MB/s) - ‘fixme1.py’ saved [837/837]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
fixme1.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 fixme1.py   
  File "/home/kali/Desktop/picoCTF/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ nano fixme1.py    

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 
```
## Notas adicionales
## Referencias