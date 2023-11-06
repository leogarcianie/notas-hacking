# basic-mod1
## Objetivo
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/128/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
## Solución
```
┌──(kali㉿kali)-[~]
└─$ wget 'https://artifacts.picoctf.net/c/128/message.txt'                           
--2023-11-06 16:53:27--  https://artifacts.picoctf.net/c/128/message.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.104, 18.154.144.85, 18.154.144.107, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 84 [application/octet-stream]
Saving to: ‘message.txt’

message.txt                                100%[======================================================================================>]      84  --.-KB/s    in 0s      

2023-11-06 16:53:28 (3.57 MB/s) - ‘message.txt’ saved [84/84]

┌──(kali㉿kali)-[~]
└─$ cat message.txt
165 248 94 346 299 73 198 221 313 137 205 87 336 110 186 69 223 213 216 216 177 138     

┌──(kali㉿kali)-[~]
└─$ nano flag.py

┌──(kali㉿kali)-[~]
└─$ cat flag.py    
datos = open('message.txt').read().split()

flag = ''

for n in datos:
        c = int(n) % 37
        if c >= 0 and c <= 25:
                s = chr(c+65)
        elif c >= 26 and c <= 35:
                s = chr(c+22)
        else:
                s = '_'
        flag += s

print(f"picoCTF{{{flag}}}")

┌──(kali㉿kali)-[~]
└─$ python3 flag.py
picoCTF{R0UND_N_R0UND_B6B25531}
```
## Notas adicionales
## Referencias