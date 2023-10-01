# Codebook
## Objetivo
Run the Python script `code.py` in the same directory as `codebook.txt`.
- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://artifacts.picoctf.net/c/1/code.py                                               
--2023-10-01 01:17:03--  https://artifacts.picoctf.net/c/1/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.74, 18.154.132.32, 18.154.132.88, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: ‘code.py’

code.py                     100%[==========================================>]   1.25K  --.-KB/s    in 0.001s  

2023-10-01 01:17:04 (1.37 MB/s) - ‘code.py’ saved [1278/1278]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://artifacts.picoctf.net/c/1/codebook.txt
--2023-10-01 01:17:14--  https://artifacts.picoctf.net/c/1/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.74, 18.154.132.32, 18.154.132.88, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: ‘codebook.txt’

codebook.txt                100%[==========================================>]      27  --.-KB/s    in 0s      

2023-10-01 01:17:15 (29.3 MB/s) - ‘codebook.txt’ saved [27/27]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls                 
codebook.txt  code.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 code.py        
picoCTF{c0d3b00k_455157_d9aa2df2}

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 
```
## Notas adicionales
## Referencias