# GDB baby step 1
## Objetivo
Can you figure out what is in the `eax` register at the end of the `main` function? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Disassemble [this](https://artifacts.picoctf.net/c/512/debugger0_a).
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://artifacts.picoctf.net/c/512/debugger0_a'
--2023-11-17 15:46:32--  https://artifacts.picoctf.net/c/512/debugger0_a
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.104, 18.154.144.107, 18.154.144.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16472 (16K) [application/octet-stream]
Saving to: ‘debugger0_a’

debugger0_a                         100%[=================================================================>]  16.09K  --.-KB/s    in 0s      

2023-11-17 15:46:33 (38.6 MB/s) - ‘debugger0_a’ saved [16472/16472]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ gdb ./debugger0_a
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
Reading symbols from ./debugger0_a...
(No debugging symbols found in ./debugger0_a)
(gdb) run
Starting program: /home/kali/Desktop/picoCTF/debugger0_a 
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".
[Inferior 1 (process 31201) exited with code 0102]
(gdb) break *main+48
Breakpoint 1 at 0x555555555159
(gdb) continue
The program is not being run.
(gdb) print $eax
No registers.
(gdb) run
Starting program: /home/kali/Desktop/picoCTF/debugger0_a 
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".

Breakpoint 1, 0x0000555555555159 in __libc_csu_init ()
(gdb) continue
Continuing.
[Inferior 1 (process 31431) exited with code 0102]
(gdb) print $eax
$1 = -134585568
(gdb) continue
Continuing.
[Inferior 1 (process 31656) exited with code 0102]
(gdb) print $eax
No registers.
(gdb) disassemble main
Dump of assembler code for function main:
   0x0000555555555129 <+0>:     endbr64
   0x000055555555512d <+4>:     push   %rbp
   0x000055555555512e <+5>:     mov    %rsp,%rbp
   0x0000555555555131 <+8>:     mov    %edi,-0x4(%rbp)
   0x0000555555555134 <+11>:    mov    %rsi,-0x10(%rbp)
   0x0000555555555138 <+15>:    mov    $0x86342,%eax
   0x000055555555513d <+20>:    pop    %rbp
   0x000055555555513e <+21>:    ret
End of assembler dump.
(gdb) break *main+21
Breakpoint 2 at 0x55555555513e
(gdb) run
Starting program: /home/kali/Desktop/picoCTF/debugger0_a 
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".

Breakpoint 1, 0x0000555555555159 in __libc_csu_init ()
(gdb) continue
Continuing.

Breakpoint 2, 0x000055555555513e in main ()
(gdb) print $eax
$2 = 549698
(gdb) exit
A debugging session is active.

        Inferior 1 [process 32034] will be killed.

Quit anyway? (y or n) y

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 

picoctf{549698}
```
## Notas adicionales
## Referencias