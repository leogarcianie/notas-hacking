# Vigenere
## Objetivo
Can you decrypt this message? Decrypt this [message](https://artifacts.picoctf.net/c/160/cipher.txt) using this key "CYLAB".
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://artifacts.picoctf.net/c/160/cipher.txt' 
--2023-11-15 18:37:21--  https://artifacts.picoctf.net/c/160/cipher.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.104, 18.154.144.85, 18.154.144.103, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 43 [application/octet-stream]
Saving to: ‘cipher.txt’

cipher.txt                          100%[=================================================================>]      43  --.-KB/s    in 0s      

2023-11-15 18:37:21 (1.67 MB/s) - ‘cipher.txt’ saved [43/43]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat cipher.txt  
rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_2951c89f}

La pista que nos da este reto es el Vigenère cipher, entonces entonctré un decodificador de este tipo de cifrando, y en la descripción del reto nos indica que usemos la llave "CYLAB", y así obtuve la bandera:

picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_2951a89h}
```
## Notas adicionales
## Referencias
https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher
https://www.dcode.fr/cifrado-vigenere