# Glitch Cat
## Objetivo
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 55826`
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ nc saturn.picoctf.net 55826
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3          
Python 3.11.4 (main, Jun  7 2023, 10:13:09) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print('picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}')
picoCTF{gl17ch_m3_n07_9c42a45d}
>>> exit()

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 
```
## Notas adicionales
## Referencias