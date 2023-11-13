# reverse_cipher
## Objetivo
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev_this). Can you reverse the flag.
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev'
--2023-11-13 15:42:06--  https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16856 (16K) [application/octet-stream]
Saving to: ‘rev’

rev                              100%[=========================================================>]  16.46K  --.-KB/s    in 0s      

2023-11-13 15:42:07 (180 MB/s) - ‘rev’ saved [16856/16856]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev_this'
--2023-11-13 15:42:14--  https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev_this
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 24 [application/octet-stream]
Saving to: ‘rev_this’

rev_this                         100%[=========================================================>]      24  --.-KB/s    in 0s      

2023-11-13 15:42:15 (23.0 MB/s) - ‘rev_this’ saved [24/24]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ghidra   
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat rev_this
picoCTF{w1{1wq84fb<1>49}                                                                                                                                               
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ nano exp.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat exp.py       
cifrado = open ('rev_this','r').read()
print(cifrado)

flag = ''

for i in range (8, len(cifrado)-1):
        if i & 1 == 0:
                flag += chr( ord(cifrado[i]) - 5)
        else:
                flag += chr( ord(cifrado[i]) + 2)

print(flag)

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 exp.py 
picoCTF{w1{1wq84fb<1>49}
r3v3rs36ad73964

picoCTF{r3v3rs36ad73964}
```
## Notas adicionales
## Referencias