# Mr-Worldwide
## Objetivo
A musician left us a [message](https://jupiter.challenges.picoctf.org/static/d5570d48262dbba2a31f2a940409ad9d/message.txt). What's it mean?
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/d5570d48262dbba2a31f2a940409ad9d/message.txt'
--2023-11-15 18:46:39--  https://jupiter.challenges.picoctf.org/static/d5570d48262dbba2a31f2a940409ad9d/message.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 278 [application/octet-stream]
Saving to: ‘message.txt’

message.txt                         100%[=================================================================>]     278  --.-KB/s    in 0s      

2023-11-15 18:46:39 (2.71 MB/s) - ‘message.txt’ saved [278/278]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat message.txt 
picoCTF{(35.028309, 135.753082)(46.469391, 30.740883)(39.758949, -84.191605)(41.015137, 28.979530)(24.466667, 54.366669)(3.140853, 101.693207)_(9.005401, 38.763611)(-3.989038, -79.203560)(52.377956, 4.897070)(41.085651, -73.858467)(57.790001, -152.407227)(31.205753, 29.924526)}

El mensaje nos da coordenadas, y al investigar me dio las siguientes ciudades:
Kyoto, Japón
Odesa, Ucrania
Dayton, Estados Unidos
Istanbul, Turquía
Abu Dhabi, Emiratos Arabes Unidos
Kuala Lumpur, Malasia
_
Addis Abeba, Etiopía
Loja, Ecuador
Amsterdam, Holanda
Sleepy Hollow, Estados Unidos
Kodiak, Estados Unidos
Alexandria, Egipto

Entonces solo puse la inicial de cada ciudad, e incluí el guión, y así obtuve la bandera:

picoctf{kodiak_alaska}
```
## Notas adicionales
## Referencias