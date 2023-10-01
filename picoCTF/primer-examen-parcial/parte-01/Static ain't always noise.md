# Static ain't always noise
## Objetivo
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/static)? This [BASH script](https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/ltdis.sh) might help!
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/static
--2023-09-30 21:10:19--  https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: ‘static’

static                      100%[===========================================>]   8.18K  --.-KB/s    in 0s      

2023-09-30 21:10:20 (21.3 MB/s) - ‘static’ saved [8376/8376]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/ltdis.sh
--2023-09-30 21:10:31--  https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: ‘ltdis.sh’

ltdis.sh                    100%[===========================================>]     785  --.-KB/s    in 0s      

2023-09-30 21:10:32 (6.91 MB/s) - ‘ltdis.sh’ saved [785/785]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ls
ltdis.sh  static

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat ltdis.sh  
#!/bin/bash



echo "Attempting disassembly of $1 ..."


#This usage of "objdump" disassembles all (-D) of the first file given by 
#invoker, but only prints out the ".text" section (-j .text) (only section
#that matters in almost any compiled program...

objdump -Dj .text $1 > $1.ltdis.x86_64.txt


#Check that $1.ltdis.x86_64.txt is non-empty
#Continue if it is, otherwise print error and eject

if [ -s "$1.ltdis.x86_64.txt" ]
then
        echo "Disassembly successful! Available at: $1.ltdis.x86_64.txt"

        echo "Ripping strings from binary with file offsets..."
        strings -a -t x $1 > $1.ltdis.strings.txt
        echo "Any strings found in $1 have been written to $1.ltdis.strings.txt with file offset"



else
        echo "Disassembly failed!"
        echo "Usage: ltdis.sh <program-file>"
        echo "Bye!"
fi

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ chmod 777 ltdis.sh

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ ./ltdis.sh static 
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat static.ltdis.strings.txt | grep pico
   1020 picoCTF{d15a5m_t34s3r_ccb2b43e}

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 
```
## Notas adicionales
## Referencias