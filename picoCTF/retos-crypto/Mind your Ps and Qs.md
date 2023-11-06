# Mind your Ps and Qs
## Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/38f30029ab93478310e906d3d084a4c1/values)
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://mercury.picoctf.net/static/38f30029ab93478310e906d3d084a4c1/values'
--2023-11-06 16:44:54--  https://mercury.picoctf.net/static/38f30029ab93478310e906d3d084a4c1/values
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 205 [application/octet-stream]
Saving to: ‘values’

values                           100%[========================================================>]     205  --.-KB/s    in 0s      

2023-11-06 16:44:55 (113 MB/s) - ‘values’ saved [205/205]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat values                        
Decrypt my super sick RSA:
c: 240986837130071017759137533082982207147971245672412893755780400885108149004760496
n: 831416828080417866340504968188990032810316193533653516022175784399720141076262857
e: 65537

┌──(kali㉿kali)-[~]
└─$ python3
Python 3.11.4 (main, Jun  7 2023, 10:13:09) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> c=240986837130071017759137533082982207147971245672412893755780400885108149004760496
>>> e=65537
>>> p=1593021310640923782355996681284584012117
>>> q=521911930824021492581321351826927897005221
>>> n = p * q
>>> n
831416828080417866340504968188990032810316193533653516022175784399720141076262857
>>> tn = (p-1)*(q-1)
>>> d = inverse(e,tn)
>>> m = pow(c,d,n)
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_23540368}'
>>> 
```
## Notas adicionales
## Referencias