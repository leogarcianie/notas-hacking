# WebNet0
## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap'  
--2023-10-27 18:14:32--  https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 13163 (13K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap                     100%[========================================================>]  12.85K  --.-KB/s    in 0s      

2023-10-27 18:14:33 (67.0 MB/s) - ‘capture.pcap’ saved [13163/13163]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key'
--2023-10-27 18:14:42--  https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1704 (1.7K) [application/octet-stream]
Saving to: ‘picopico.key’

picopico.key                     100%[========================================================>]   1.66K  --.-KB/s    in 0.001s  

2023-10-27 18:14:43 (1.90 MB/s) - ‘picopico.key’ saved [1704/1704]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls -la
total 48
drwxr-xr-x 2 kali kali 24576 Oct 27 18:14 .
drwxr-xr-x 3 kali kali  4096 Sep 30 20:43 ..
-rw-r--r-- 1 kali kali 13163 Oct 26  2020 capture.pcap
-rw-r--r-- 1 kali kali  1704 Oct 26  2020 picopico.key

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ssldump -r capture.pcap -k picopico.key -d | grep picoCTF{ -A 2 -B 2
    0a 43 6f 6e 74 65 6e 74 2d 45 6e 63 6f 64 69 6e    .Content-Encodin
    67 3a 20 67 7a 69 70 0d 0a 50 69 63 6f 2d 46 6c    g: gzip..Pico-Fl
    61 67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67    ag: picoCTF{nong
    73 68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63    shim.shrimp.crac
    6b 65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c    kers}..Content-L
--
    43 6f 6e 74 65 6e 74 2d 45 6e 63 6f 64 69 6e 67    Content-Encoding
    3a 20 67 7a 69 70 0d 0a 50 69 63 6f 2d 46 6c 61    : gzip..Pico-Fla
    67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67 73    g: picoCTF{nongs
    68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63 6b    him.shrimp.crack
    65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c 65    ers}..Content-Le

picoCTF{nongshim.shrimp.crackers}
```
## Notas adicionales
## Referencias