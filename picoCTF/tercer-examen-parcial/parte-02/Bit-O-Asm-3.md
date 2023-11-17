# Bit-O-Asm-3
## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt).
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt'
--2023-11-17 14:57:14--  https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.85, 18.154.144.107, 18.154.144.104, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 461 [application/octet-stream]
Saving to: ‘disassembler-dump0_c.txt’

disassembler-dump0_c.txt            100%[=================================================================>]     461  --.-KB/s    in 0s      

2023-11-17 14:57:15 (124 MB/s) - ‘disassembler-dump0_c.txt’ saved [461/461]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat disassembler-dump0_c.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0xc],0x9fe1a
<+22>:    mov    DWORD PTR [rbp-0x8],0x4
<+29>:    mov    eax,DWORD PTR [rbp-0xc]
<+32>:    imul   eax,DWORD PTR [rbp-0x8]
<+36>:    add    eax,0x1f5
<+41>:    mov    DWORD PTR [rbp-0x4],eax
<+44>:    mov    eax,DWORD PTR [rbp-0x4]
<+47>:    pop    rbp
<+48>:    ret

Luego de analizar el complicado código obtuve el valor "0x9fe1a" el cual equivale a 654874 y venía de [rbp-0xc]. Después lo multipliqué por "0x4" = 4, que venía de [rbp-0x8], y por último le sume el valor de "0x1f5" = 501, que venía del eax "normal", y así obtuve la bandera:
(654874 * 4) + 501 = 2619997
picoctf{2619997}
```
## Notas adicionales
## Referencias