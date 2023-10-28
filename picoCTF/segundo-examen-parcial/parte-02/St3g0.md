# St3g0
## Objetivo
Download this image and find the flag.
- [Download image](https://artifacts.picoctf.net/c/217/pico.flag.png)
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://artifacts.picoctf.net/c/217/pico.flag.png'                   
--2023-10-28 19:01:33--  https://artifacts.picoctf.net/c/217/pico.flag.png
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.104, 18.154.144.85, 18.154.144.107, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 13443 (13K) [application/octet-stream]
Saving to: ‘pico.flag.png’

pico.flag.png                    100%[========================================================>]  13.13K  --.-KB/s    in 0s      
2023-10-28 19:01:34 (142 MB/s) - ‘pico.flag.png’ saved [13443/13443]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ sudo gem install zsteg
[sudo] password for kali: 
Fetching rainbow-3.1.1.gem
Fetching iostruct-0.0.5.gem
Fetching zsteg-0.2.13.gem
Fetching zpng-0.4.5.gem
Successfully installed rainbow-3.1.1
Successfully installed zpng-0.4.5
Successfully installed iostruct-0.0.5
Successfully installed zsteg-0.2.13
Parsing documentation for rainbow-3.1.1
Installing ri documentation for rainbow-3.1.1
Parsing documentation for zpng-0.4.5
Installing ri documentation for zpng-0.4.5
Parsing documentation for iostruct-0.0.5
Installing ri documentation for iostruct-0.0.5
Parsing documentation for zsteg-0.2.13
Installing ri documentation for zsteg-0.2.13
Done installing documentation for rainbow, zpng, iostruct, zsteg after 0 seconds
4 gems installed

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ zsteg pico.flag.png
b1,r,lsb,xy         .. text: "~__B>VG?G@"
b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_a9a181eb}$t3g0"
b1,abgr,lsb,xy      .. text: "E2A5q4E%uSA"
b2,b,lsb,xy         .. text: "AAPAAQTAAA"
b2,b,msb,xy         .. text: "HWUUUUUU"
b3,r,lsb,xy         .. file: gfxboot compiled html help file
b4,r,lsb,xy         .. file: Targa image data (16-273) 65536 x 4097 x 1 +4352 +4369 - 1-bit alpha - right "\021\020\001\001\021\021\001\001\021\021\001"                                                                                                            
b4,g,lsb,xy         .. file: 0420 Alliant virtual executable not stripped
b4,b,lsb,xy         .. file: Targa image data - Map 272 x 17 x 16 +257 +272 - 1-bit alpha "\020\001\021\001\021\020\020\001\020\001\020\001"                                                                                                                        
b4,bgr,lsb,xy       .. file: Targa image data - Map 273 x 272 x 16 +1 +4113 - 1-bit alpha "\020\001\001\001"
b4,rgba,msb,xy      .. file: Applesoft BASIC program data, first line number 8

picoCTF{7h3r3_15_n0_5p00n_a9a181eb}
```
## Notas adicionales
## Referencias