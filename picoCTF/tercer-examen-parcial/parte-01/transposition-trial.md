# transposition-trial
## Objetivo
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message. Download the corrupted message [here](https://artifacts.picoctf.net/c/191/message.txt).
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://artifacts.picoctf.net/c/191/message.txt'                                              
--2023-11-15 18:27:23--  https://artifacts.picoctf.net/c/191/message.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.85, 18.154.144.104, 18.154.144.107, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 54 [application/octet-stream]
Saving to: ‘message.txt’

message.txt                         100%[=================================================================>]      54  --.-KB/s    in 0s      

2023-11-15 18:27:24 (25.2 MB/s) - ‘message.txt’ saved [54/54]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat message.txt 
heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V6E5926A}4                   

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ nano flag.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat flag.py    
message = "heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V6E5926A}4"
flag = ""
for i in range(len(message)):
    if i % 3 == 0:
        flag = flag + message[i+2] + message[i]
    elif i % 3 == 2:
        pass
    else:
        flag = flag + message[i]
print(flag)

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 flag.py
The flag is picoCTF{7R4N5P051N6_15_3XP3N51V3_56E6924A}

Al momento de leer el mensaje me di cuenta que tenía algún tipo de cifrado, y después de analizarlo me di cuenta que en cada 3 caracteres la letra se va al final, entonces hice un script de python para hacerlo automaticamente, y asi obtuve la bandera:

picoCTF{7R4N5P051N6_15_3XP3N51V3_56E6924A}
```
## Notas adicionales
## Referencias