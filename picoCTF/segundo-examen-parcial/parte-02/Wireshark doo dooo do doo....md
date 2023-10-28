# Wireshark doo dooo do doo...
## Objetivo
Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/d6f9aa16d2a2c51d2e431e658d87af9e/shark1.pcapng).
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://mercury.picoctf.net/static/d6f9aa16d2a2c51d2e431e658d87af9e/shark1.pcapng'
--2023-10-28 18:45:36--  https://mercury.picoctf.net/static/d6f9aa16d2a2c51d2e431e658d87af9e/shark1.pcapng
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1558808 (1.5M) [application/octet-stream]
Saving to: ‘shark1.pcapng’

shark1.pcapng                    100%[========================================================>]   1.49M   901KB/s    in 1.7s    

2023-10-28 18:45:38 (901 KB/s) - ‘shark1.pcapng’ saved [1558808/1558808]

┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wireshark shark1.pcapng

Después de entrar a wireshark vamos a los archivos TCP y ahi en el stream 5 se encuentra lo siguiente:

GET / HTTP/1.1
Host: 18.222.37.134
Connection: keep-alive
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.105 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9

HTTP/1.1 200 OK
Date: Mon, 10 Aug 2020 01:51:45 GMT
Server: Apache/2.4.29 (Ubuntu)
Last-Modified: Fri, 07 Aug 2020 00:45:02 GMT
ETag: "2f-5ac3eea4fcf01"
Accept-Ranges: bytes
Content-Length: 47
Keep-Alive: timeout=5, max=100
Connection: Keep-Alive
Content-Type: text/html

Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}

La bandera está encriptada en ROT13, una ves desencriptada nos da la bandera:
The flag is picoCTF{p33kab00_1_s33_u_deadbeef}
```
## Notas adicionales
## Referencias