# Lookey here
## Objetivo
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it. Download the data [here](https://artifacts.picoctf.net/c/126/anthem.flag.txt).
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://artifacts.picoctf.net/c/126/anthem.flag.txt' 
--2023-10-28 18:53:34--  https://artifacts.picoctf.net/c/126/anthem.flag.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.103, 18.154.144.85, 18.154.144.107, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.103|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108668 (106K) [application/octet-stream]
Saving to: ‘anthem.flag.txt’

anthem.flag.txt                  100%[========================================================>] 106.12K   704KB/s    in 0.2s    

2023-10-28 18:53:34 (704 KB/s) - ‘anthem.flag.txt’ saved [108668/108668]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
anthem.flag.txt

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat anthem.flag.txt | grep picoCTF
      we think that the men of picoCTF{gr3p_15_@w3s0m3_2116b979}
```
## Notas adicionales
## Referencias