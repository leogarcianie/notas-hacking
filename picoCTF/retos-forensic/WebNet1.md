# WebNet1
## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap'
--2023-10-27 18:17:02--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 92525 (90K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap                     100%[========================================================>]  90.36K   427KB/s    in 0.2s    

2023-10-27 18:17:03 (427 KB/s) - ‘capture.pcap’ saved [92525/92525]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key'
--2023-10-27 18:17:14--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1704 (1.7K) [application/octet-stream]
Saving to: ‘picopico.key’

picopico.key                     100%[========================================================>]   1.66K  --.-KB/s    in 0s      
2023-10-27 18:17:15 (38.7 MB/s) - ‘picopico.key’ saved [1704/1704]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
capture.pcap  picopico.key

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wireshark capture.pcap
 ** (wireshark:2416) 21:40:53.977175 [GUI WARNING] -- FIX Add drag reordering to UAT dialog
 ** (wireshark:2416) 21:41:36.419489 [GUI WARNING] -- QXcbConnection: XCB error: 3 (BadWindow), sequence: 5280, resource id: 20988468, major code: 40 (TranslateCoords), minor code: 0
^C

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
capture.pcap  picopico.key  vulture.jpg

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ open vulture.jpg

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ strings vulture.jpg -n15
picoCTF{honey.roasted.peanuts}
 )/'%'/9339GDG]]}
 )/'%'/9339GDG]]}
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
```
## Notas adicionales
## Referencias