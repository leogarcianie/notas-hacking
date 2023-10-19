# WhitePages
## Objetivo
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt) is all blank!
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 -m pip install pwntools                                                     ...            
Successfully installed capstone-5.0.1 colored-traceback-0.3.0 intervaltree-3.1.0 plumbum-1.8.2 pwntools-4.11.0 pyelftools-0.30 ropgadget-7.4 rpyc-5.3.1 unicorn-2.0.1.post1

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ nano flag.py                                    

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat flag.py 
from pwn import *
file = open('whitepages.txt','rb')
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83',b'0')
data = data.replace(b'\x20',b'1')
data = data.decode('ascii')
data = unbits(data)
print(data)

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python flag.py                 
b'\n\t\tpicoCTF\n\n\t\tSEE PUBLIC RECORDS & BACKGROUND REPORT\n\t\t5000 Forbes Ave, Pittsburgh, PA 15213\n\t\tpicoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}\n\t\t'

picoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}
```
## Notas adicionales
## Referencias