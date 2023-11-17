# GDB baby step 2
## Objetivo
Can you figure out what is in the `eax` register at the end of the `main` function? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Debug [this](https://artifacts.picoctf.net/c/520/debugger0_b).
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://artifacts.picoctf.net/c/520/debugger0_b'
--2023-11-17 15:47:28--  https://artifacts.picoctf.net/c/520/debugger0_b
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.104, 18.154.144.107, 18.154.144.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16304 (16K) [application/octet-stream]
Saving to: ‘debugger0_b’

debugger0_b                         100%[=================================================================>]  15.92K  --.-KB/s    in 0.008s  

2023-11-17 15:47:29 (1.89 MB/s) - ‘debugger0_b’ saved [16304/16304]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ chmod +x debugger0_b

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ gdb ./debugger0_b
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
Reading symbols from ./debugger0_b...
(No debugging symbols found in ./debugger0_b)
(gdb) disassemble main
Dump of assembler code for function main:
   0x0000000000401106 <+0>:     endbr64
   0x000000000040110a <+4>:     push   %rbp
   0x000000000040110b <+5>:     mov    %rsp,%rbp
   0x000000000040110e <+8>:     mov    %edi,-0x14(%rbp)
   0x0000000000401111 <+11>:    mov    %rsi,-0x20(%rbp)
   0x0000000000401115 <+15>:    movl   $0x1e0da,-0x4(%rbp)
   0x000000000040111c <+22>:    movl   $0x25f,-0xc(%rbp)
   0x0000000000401123 <+29>:    movl   $0x0,-0x8(%rbp)
   0x000000000040112a <+36>:    jmp    0x401136 <main+48>
   0x000000000040112c <+38>:    mov    -0x8(%rbp),%eax
   0x000000000040112f <+41>:    add    %eax,-0x4(%rbp)
   0x0000000000401132 <+44>:    addl   $0x1,-0x8(%rbp)
   0x0000000000401136 <+48>:    mov    -0x8(%rbp),%eax
   0x0000000000401139 <+51>:    cmp    -0xc(%rbp),%eax
   0x000000000040113c <+54>:    jl     0x40112c <main+38>
   0x000000000040113e <+56>:    mov    -0x4(%rbp),%eax
   0x0000000000401141 <+59>:    pop    %rbp
   0x0000000000401142 <+60>:    ret
End of assembler dump.
(gdb) break *main+60
Breakpoint 1 at 0x401142
(gdb) run
Starting program: /home/kali/Desktop/picoCTF/debugger0_b 
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".

Breakpoint 1, 0x0000000000401142 in main ()
(gdb) print $eax
$1 = 307019
(gdb) quit
A debugging session is active.

        Inferior 1 [process 33941] will be killed.

Quit anyway? (y or n) y

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 

picoctf{307019}
```
## Notas adicionales
## Referencias