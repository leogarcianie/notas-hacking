# Wave a flag
## Objetivo
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm) has extraordinarily helpful information...
## Solución
```                                                                                 
┌──(kali㉿kali)-[~]
└─$ wget https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm
--2023-09-30 20:34:04--  https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: ‘warm’

warm                  100%[=======================>]  10.68K  --.-KB/s    in 0s      

2023-09-30 20:34:05 (22.9 MB/s) - ‘warm’ saved [10936/10936]

                                                                                      
┌──(kali㉿kali)-[~]
└─$ ls                      
Desktop    Downloads  hacking  Pictures  Templates  warm
Documents  flag       Music    Public    Videos
                                                                                      
┌──(kali㉿kali)-[~]
└─$ chmod 777 warm
                                                                                      
┌──(kali㉿kali)-[~]
└─$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}
                                                                                      
┌──(kali㉿kali)-[~]
└─$ 
```
## Notas adicionales
## Referencias