# Nice netcat...
## Objetivo
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 22902`, but it doesn't speak English...
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ nc mercury.picoctf.net 22902
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
100 
51 
100 
102 
100 
54 
100 
102 
125 
10 

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ nano nicenetcat.py          

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ cat nicenetcat.py
nums = [112, 105, 99 111, 67, 84, 70, 123, 103, 48, 48, 100, 95, 107, 49, 116, 116, 121, 33, 95, 110, 49, 99, 51, 95, 107, 49, 116, 116, 121, 33, 95, 100, 51, 100, 102, 100, 54, 100, 102, 125, 10]
flag = ""
for number in nums:
    flag += chr(number)
print(flag)

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ python3 nicenetcat.py
picoCTF{g00d_k1tty!_n1c3_k1tty!_d3dfd6df}

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ 
```
## Notas adicionales
## Referencias