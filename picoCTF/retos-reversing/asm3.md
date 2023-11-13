# asm3
## Objetivo
What does asm3(0xd73346ed,0xd48672ae,0xd3c8b139) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/17c5620fcffa388fe518d31cb4dd99a0/test.S)
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/17c5620fcffa388fe518d31cb4dd99a0/test.S'
--2023-11-13 15:20:23--  https://jupiter.challenges.picoctf.org/static/17c5620fcffa388fe518d31cb4dd99a0/test.S
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 286 [application/octet-stream]
Saving to: ‘test.S’

test.S                           100%[==========================================================>]     286  --.-KB/s    in 0s      

2023-11-13 15:20:24 (2.48 MB/s) - ‘test.S’ saved [286/286]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat test.S         
asm3:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   xor    eax,eax
        <+5>:   mov    ah,BYTE PTR [ebp+0xa]
        <+8>:   shl    ax,0x10
        <+12>:  sub    al,BYTE PTR [ebp+0xc]
        <+15>:  add    ah,BYTE PTR [ebp+0xd]
        <+18>:  xor    ax,WORD PTR [ebp+0x10]
        <+22>:  nop
        <+23>:  pop    ebp
        <+24>:  ret    

EAX 0x0000C36B  EBX 0x00000000
ECX 0x00000000  EDX 0x00000000
ESI 0x00000000  EDI 0x00000000
EBP 0x000203EC  ESP 0x000203EC
EIP 0x00020430 Ln 16, Col 9
Flags
Carry 0  Dir      0
Int   0  Overflow 0
Sign  1  Zero     0

0xC36B
```
## Notas adicionales
## Referencias
https://carlosrafaelgn.com.br/Asm86/