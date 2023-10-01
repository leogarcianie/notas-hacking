# runme.py
## Objetivo
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://artifacts.picoctf.net/c/34/runme.py       
--2023-10-01 02:19:32--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.32, 18.154.132.108, 18.154.132.88, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.32|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: ‘runme.py’

runme.py                    100%[==========================================>]     270  --.-KB/s    in 0s      

2023-10-01 02:19:33 (85.5 MB/s) - ‘runme.py’ saved [270/270]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
runme.py

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 runme.py 
picoCTF{run_s4n1ty_run}

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 
```
## Notas adicionales
## Referencias