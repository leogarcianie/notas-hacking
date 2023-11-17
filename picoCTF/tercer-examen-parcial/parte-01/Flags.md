# Flags
## Objetivo
What do the [flags](https://jupiter.challenges.picoctf.org/static/fbeb5f9040d62b18878d199cdda2d253/flag.png) mean?
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/fbeb5f9040d62b18878d199cdda2d253/flag.png'
--2023-11-15 18:41:49--  https://jupiter.challenges.picoctf.org/static/fbeb5f9040d62b18878d199cdda2d253/flag.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 43257 (42K) [application/octet-stream]
Saving to: ‘flag.png’

flag.png                            100%[=================================================================>]  42.24K  --.-KB/s    in 0.1s    

2023-11-15 18:41:50 (385 KB/s) - ‘flag.png’ saved [43257/43257]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ open flag.png 

Siguiendo el patrón de la imagen como ya se sabía que empazaba con "picoCTF", convertí las banderas que se repetían y me dio como resultado lo siguiente:

picoctf{f----------ff}

Después de invertigar sobre las banderas, entontré las banderas de señales maritimas, y así pude resolverlo, dando como resultado la bandera:

picoctf{f1ag5and5tuff}
```
## Notas adicionales
## Referencias