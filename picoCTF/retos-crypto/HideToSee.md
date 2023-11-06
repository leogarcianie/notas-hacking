# HideToSee
## Objetivo
How about some hide and seek heh? Look at this image [here](https://artifacts.picoctf.net/c/235/atbash.jpg).
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://artifacts.picoctf.net/c/235/atbash.jpg'
--2023-11-06 17:03:06--  https://artifacts.picoctf.net/c/235/atbash.jpg
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.85, 18.154.144.107, 18.154.144.104, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 51499 (50K) [application/octet-stream]
Saving to: ‘atbash.jpg.1’

atbash.jpg.1                          100%[========================================================================>]  50.29K  --.-KB/s    in 0.05s   

2023-11-06 17:03:07 (946 KB/s) - ‘atbash.jpg.1’ saved [51499/51499]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ steghide extract -sf atbash.jpg
Enter passphrase: 
wrote extracted data to "encrypted.txt".

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_92533667}

Convertimos la bandera en: https://www.dcode.fr/atbash-cipher

picoCTF{atbash_crack_92533667}
```
## Notas adicionales
## Referencias