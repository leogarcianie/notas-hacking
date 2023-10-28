# Packets Primer
## Objetivo
Download the packet capture file and use packet analysis software to find the flag.
- [Download packet capture](https://artifacts.picoctf.net/c/196/network-dump.flag.pcap)
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://artifacts.picoctf.net/c/196/network-dump.flag.pcap'
--2023-10-28 18:56:12--  https://artifacts.picoctf.net/c/196/network-dump.flag.pcap
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.104, 18.154.144.103, 18.154.144.107, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 778 [application/octet-stream]
Saving to: ‘network-dump.flag.pcap’

network-dump.flag.pcap           100%[========================================================>]     778  --.-KB/s    in 0s      

2023-10-28 18:56:12 (7.69 MB/s) - ‘network-dump.flag.pcap’ saved [778/778]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ssldump -r network-dump.flag.pcap -d
New TCP connection #1: 10.0.2.15(48750) <-> 10.0.2.4(9000)
0.0012 (0.0012)  C>S
---------------------------------------------------------------
p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ 0 1 b 0 a 0 d 6 }
---------------------------------------------------------------

Cleaned 1 remaining connection(s) from connection pool

picoCTF{p4ck37_5h4rk_01b0a0d6}
```
## Notas adicionales
## Referencias