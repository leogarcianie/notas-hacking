# strings it
## Objetivo
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
--2023-10-01 01:37:32--  https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: ‘strings’

strings                     100%[==========================================>] 757.84K   939KB/s    in 0.8s    

2023-10-01 01:37:34 (939 KB/s) - ‘strings’ saved [776032/776032]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
strings

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ mv strings otro

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
otro

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ strings otro | grep pico
picoCTF{5tRIng5_1T_d66c7bb7}

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 
```
## Notas adicionales
## Referencias