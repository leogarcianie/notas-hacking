# ASCII FTW
## Objetivo
This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program. You can download the file from [here](https://artifacts.picoctf.net/c/508/asciiftw).
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://artifacts.picoctf.net/c/508/asciiftw'                                              
--2023-11-17 14:40:10--  https://artifacts.picoctf.net/c/508/asciiftw
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.104, 18.154.144.107, 18.154.144.103, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16752 (16K) [application/octet-stream]
Saving to: ‘asciiftw’

asciiftw                            100%[=================================================================>]  16.36K  --.-KB/s    in 0.01s   

2023-11-17 14:40:11 (1.33 MB/s) - ‘asciiftw’ saved [16752/16752]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ gdb asciiftw      
GNU gdb (Debian 13.2-1) 13.2
Copyright (C) 2023 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from asciiftw...
(No debugging symbols found in asciiftw)
(gdb) disassemble main
Dump of assembler code for function main:
   0x0000000000001169 <+0>:     endbr64
   0x000000000000116d <+4>:     push   %rbp
   0x000000000000116e <+5>:     mov    %rsp,%rbp
   0x0000000000001171 <+8>:     sub    $0x30,%rsp
   0x0000000000001175 <+12>:    mov    %fs:0x28,%rax
   0x000000000000117e <+21>:    mov    %rax,-0x8(%rbp)
   0x0000000000001182 <+25>:    xor    %eax,%eax
   0x0000000000001184 <+27>:    movb   $0x70,-0x30(%rbp)
   0x0000000000001188 <+31>:    movb   $0x69,-0x2f(%rbp)
   0x000000000000118c <+35>:    movb   $0x63,-0x2e(%rbp)
   0x0000000000001190 <+39>:    movb   $0x6f,-0x2d(%rbp)
   0x0000000000001194 <+43>:    movb   $0x43,-0x2c(%rbp)
   0x0000000000001198 <+47>:    movb   $0x54,-0x2b(%rbp)
   0x000000000000119c <+51>:    movb   $0x46,-0x2a(%rbp)
   0x00000000000011a0 <+55>:    movb   $0x7b,-0x29(%rbp)
   0x00000000000011a4 <+59>:    movb   $0x41,-0x28(%rbp)
   0x00000000000011a8 <+63>:    movb   $0x53,-0x27(%rbp)
   0x00000000000011ac <+67>:    movb   $0x43,-0x26(%rbp)
   0x00000000000011b0 <+71>:    movb   $0x49,-0x25(%rbp)
   0x00000000000011b4 <+75>:    movb   $0x49,-0x24(%rbp)
   0x00000000000011b8 <+79>:    movb   $0x5f,-0x23(%rbp)
   0x00000000000011bc <+83>:    movb   $0x49,-0x22(%rbp)
   0x00000000000011c0 <+87>:    movb   $0x53,-0x21(%rbp)
   0x00000000000011c4 <+91>:    movb   $0x5f,-0x20(%rbp)
   0x00000000000011c8 <+95>:    movb   $0x45,-0x1f(%rbp)
   0x00000000000011cc <+99>:    movb   $0x41,-0x1e(%rbp)
   0x00000000000011d0 <+103>:   movb   $0x53,-0x1d(%rbp)
   0x00000000000011d4 <+107>:   movb   $0x59,-0x1c(%rbp)
   0x00000000000011d8 <+111>:   movb   $0x5f,-0x1b(%rbp)
   0x00000000000011dc <+115>:   movb   $0x38,-0x1a(%rbp)
   0x00000000000011e0 <+119>:   movb   $0x39,-0x19(%rbp)
   0x00000000000011e4 <+123>:   movb   $0x36,-0x18(%rbp)
   0x00000000000011e8 <+127>:   movb   $0x30,-0x17(%rbp)
   0x00000000000011ec <+131>:   movb   $0x46,-0x16(%rbp)
   0x00000000000011f0 <+135>:   movb   $0x30,-0x15(%rbp)
   0x00000000000011f4 <+139>:   movb   $0x41,-0x14(%rbp)
--Type <RET> for more, q to quit, c to continue without paging--q
Quit
(gdb) quit

Después de desensamblar el programa en su función main, me doy cuenta que hay varias líneas que contienen la palabra "movb", entonces convertí los valores hexadecimales que tenía cada linea en caracteres, y así obtuve la bandera:
picoctf{ascii_is_easy_8960f0af}
```
## Notas adicionales
## Referencias