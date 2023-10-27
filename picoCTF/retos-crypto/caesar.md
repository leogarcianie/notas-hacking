# caesar
## Objetivo
Decrypt this [message](https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext).
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext'
--2023-10-27 18:41:40--  https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 35 [application/octet-stream]
Saving to: ‘ciphertext’

ciphertext                       100%[========================================================>]      35  --.-KB/s    in 0s  

2023-10-27 18:41:41 (15.7 MB/s) - ‘ciphertext’ saved [35/35]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat ciphertext  
picoCTF{ynkooejcpdanqxeykjrbdofgkq}                                                                                                                                  
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ nano flag.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat flag.py   
import string
import re
abc=string.ascii_letters
encriptado = open('ciphertext','r').read()
encriptado = re.findall('\{(.*?)\}',encriptado)[0]
rot = 25
salida = ''
for car in encriptado:
	salida += abc[ (abc.find(car) + rot) % 26 ]
print(salida)

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 flag.py

picoCTF{crossingtherubiconvfhsjkou}
```
## Notas adicionales
## Referencias