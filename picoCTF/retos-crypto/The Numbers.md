# The Numbers
## Objetivo
The [numbers](https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png)... what do they mean?
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png'
--2023-10-27 18:29:11--  https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 100721 (98K) [application/octet-stream]
Saving to: ‘the_numbers.png’

the_numbers.png                  100%[========================================================>]  98.36K   248KB/s    in 0.4s    

2023-10-27 18:29:12 (248 KB/s) - ‘the_numbers.png’ saved [100721/100721]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ open the_numbers.png  

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ nano flag.py
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat flag.py                       
entrada = input().split()
alfabeto = {'1':'a','2':'b','3':'c','4':'d','5':'e','6':'f','7':'g','8':'h','9':'i','10':'j','11':'k','12':'l','13':'m','14':'n','15':'o','16':'p','17':'q','18':'r','19':'s','20':'t','21':'u','22':'v', '23':'w','24':'x','25':'y','26':'z'}
cadena=''
for c in entrada:
        a = alfabeto.get(c)
        if(a!=None):
                cadena+=a
        else:
                cadena+=c
print(cadena.upper())            

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 flag.py
picoCTF{thenumbersmason}
```
## Notas adicionales
## Referencias