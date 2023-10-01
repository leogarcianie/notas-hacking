# Tab, Tab, Attack
## Objetivo
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip)
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip
--2023-09-30 21:21:19--  https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4520 (4.4K) [application/octet-stream]
Saving to: ‘Addadshashanammu.zip’

Addadshashanammu.zip        100%[===========================================>]   4.41K  --.-KB/s    in 0s      

2023-09-30 21:21:20 (22.3 MB/s) - ‘Addadshashanammu.zip’ saved [4520/4520]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
Addadshashanammu.zip

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ unzip Addadshashanammu.zip  

Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
Addadshashanammu  Addadshashanammu.zip

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls Addadshashanammu
Almurbalarammi

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls -R Addadshashanammu
Addadshashanammu:
Almurbalarammi

Addadshashanammu/Almurbalarammi:
Ashalmimilkala

Addadshashanammu/Almurbalarammi/Ashalmimilkala:
Assurnabitashpi

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi:
Maelkashishi

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi:
Onnissiralis

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis:
Ularradallaku

Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku:
fang-of-haynekhtnamet

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ strings Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet | grep pico
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_d32e018c}

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 
```
## Notas adicionales
## Referencias