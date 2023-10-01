# convertme.py
## Objetivo
Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)
## Solución
```           
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2023-10-01 01:21:22--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.108, 18.154.132.74, 18.154.132.32, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.108|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: ‘convertme.py’

convertme.py                100%[==========================================>]   1.16K  --.-KB/s    in 0s      

2023-10-01 01:21:23 (38.3 MB/s) - ‘convertme.py’ saved [1189/1189]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
convertme.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 convertme.py
If 30 is in decimal base, what is it in binary base?
Answer: 11110
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 
```
## Notas adicionales
## Referencias