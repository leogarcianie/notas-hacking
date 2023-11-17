# Bit-O-Asm-2
## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt'
--2023-11-17 14:50:05--  https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.85, 18.154.144.103, 18.154.144.104, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: ‘disassembler-dump0_b.txt’

disassembler-dump0_b.txt            100%[=================================================================>]     270  --.-KB/s    in 0s      

2023-11-17 14:50:06 (69.9 MB/s) - ‘disassembler-dump0_b.txt’ saved [270/270]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat disassembler-dump0_b.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a
<+22>:    mov    eax,DWORD PTR [rbp-0x4]
<+25>:    pop    rbp
<+26>:    ret

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ echo $((0x9fe1a))
654874

Después de analizar el archivo dado de este reto, encontré la línea con el valor "eax", y ahí me indica la dirección de memoria en: "[rbp-0x4]", después de buscar esto encontré la linea con este valor, y ahi me indicaba un valor hexadecimal "0x9fe1a", el cual es el valor de la bandera:
picoctf{654874}
```
## Notas adicionales
## Referencias