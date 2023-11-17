# Bit-O-Asm-1
## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt).
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt'
--2023-11-17 14:46:37--  https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.85, 18.154.144.104, 18.154.144.107, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 209 [application/octet-stream]
Saving to: ‘disassembler-dump0_a.txt’

disassembler-dump0_a.txt            100%[=================================================================>]     209  --.-KB/s    in 0.002s  

2023-11-17 14:46:38 (86.7 KB/s) - ‘disassembler-dump0_a.txt’ saved [209/209]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat disassembler-dump0_a.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x4],edi
<+11>:    mov    QWORD PTR [rbp-0x10],rsi
<+15>:    mov    eax,0x30
<+20>:    pop    rbp
<+21>:    ret

Después de analizar el código dado, encontre el valor "eax", y contenía el valor hexadecimal 0x30, el cual es igual a "48", y así obtuve la bandera:
picoctf{48}
```
## Notas adicionales
## Referencias