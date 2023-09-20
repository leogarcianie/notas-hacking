# Level 16 🡪 Level 17
## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit16
Password: JQttfApK4SeyHwDlI9SXGR50qclOAil1
```
## Solución
```
bandit16@bandit:~$ nmap -p 31000-32000 localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2023-09-20 00:32 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00050s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.06 seconds
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Sep 18 14:32:48 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Sep 18 14:32:48 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Sep 18 14:31:48 2023 GMT; NotAfter: Sep 18 14:32:48 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEb7jfsDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwOTE4MTQzMTQ4WhcNMjMwOTE4MTQzMjQ4WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDF
/JRVSGUn03lXEGF3AegYY+mPc6ZozCOGy7hYlVO0DfAtuMj3QiiwF7K3NKscjQSU
yPtOA4mfOC+QAmLSC/Kwi7GjAiPKD8u7NgjNES92o2tsfy/UKtDhYxazMFycbesh
eUvZStB7rEpWY3p4AAbVpSGnbiuriTBVNmrKqAz0dDYDFVWsS/K6isQeuahqJ/Nr
LW2WvucEHyvE49dcfc9FiQOqyeV17diRuZhV9cJGh5ld0uEHftocjFLRIWgDuLGn
EMJYPlPxmQi1aDnUU6mvtlUCFAqrMUK+svaaEMuOF6ljrgHb0NVJ7QlVwM6JCLpi
/F6eg2hLENneSkKVkwhfAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCW
cS0a0udS+PuAsBPaDO9li2pcRiiWmMFtZMjskpk7ggmu+dWwy1Hyhe15mwhtRMHc
mSIDcmpnsQhXnNdygPkASDYuBMvEF3x2lrtevEc/tsgWI0jiu4GHY9/xgV1yi0g/
/cj9uEeYZu9f742QV0XVfcVIljCSvT3Ic47MerUKttZ19RVpALuGaWk8++a535x9
gOtfFUs1LGXuphHVvB1Kdj5icD74PV1ZFXV6e7TheMUgrMjJb93T3cyM8IWIuEGu
Z/garZZVV4DetxbSioTgZx7FPdnQ+xg7/gMqsSeoV1ouTN5gEkOmva+qkk2+C+FC
jNEIr/7SZciUS0Nimpcm
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 014991A9A1201295B8AF8AF3E5E3CC9ED12EA1ABCD5594C2F7A9CC48F8DBA976
    Session-ID-ctx:
    Resumption PSK: 65DD80386CFED981AEC6328E3B65B3F6237E08D2A5AB9A94AAD38120D206DEFDCE936047F8A159437103280166A652B4
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - f1 d7 8c 2f 7c 5d 01 37-ac 93 cd d3 c4 31 18 b8   .../|].7.....1..
    0010 - 89 34 02 a8 73 4e 01 24-70 90 37 00 7a 57 eb 96   .4..sN.$p.7.zW..
    0020 - 25 86 5b 2a c6 03 fc 60-f4 5f 75 d9 e2 b0 ae 49   %.[*...`._u....I
    0030 - 16 53 3e a9 9b 61 bb 43-c4 aa 33 33 fd 14 b6 8e   .S>..a.C..33....
    0040 - 53 25 65 98 46 20 c8 93-a1 70 4c 69 bd 6e b6 8b   S%e.F ...pLi.n..
    0050 - 44 12 58 51 2b b2 43 39-5a 90 7a a7 d9 6b 20 8d   D.XQ+.C9Z.z..k .
    0060 - 7e d6 a8 a3 f2 19 20 bd-76 8f 69 33 50 a8 79 74   ~..... .v.i3P.yt
    0070 - b4 53 36 e0 3a 2a 44 9a-7d 50 06 ba d7 a1 a0 a3   .S6.:*D.}P......
    0080 - 38 36 90 af c0 ea a9 61-52 89 40 b6 fb c7 05 72   86.....aR.@....r
    0090 - da 1a 3f 4b 69 f9 8a 5a-13 44 84 23 7d 1c 35 89   ..?Ki..Z.D.#}.5.
    00a0 - 77 60 a2 cf 45 c7 01 21-31 3d 9b 6d f7 47 b2 cf   w`..E..!1=.m.G..
    00b0 - dd 47 52 7b 4f e5 25 11-5e 95 05 31 d5 ed 97 8d   .GR{O.%.^..1....
    00c0 - ab c4 2f 88 cd f6 ae cc-7c 4d 95 2a ce fd e3 ba   ../.....|M.*....

    Start Time: 1695169985
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: D0312D34FAB25848C0B070C76DE1D9EC9D795A82552DEB76E0D4E505F1484E00
    Session-ID-ctx:
    Resumption PSK: 4D7C297FF4592FD0570129C8DCB17F22C893129E2A5FEBF5E771E58191605CE61AA3A3BA582F5CB747B5520B03F4DCE6
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - f1 d7 8c 2f 7c 5d 01 37-ac 93 cd d3 c4 31 18 b8   .../|].7.....1..
    0010 - 53 38 4f 11 a7 05 e5 6e-89 4b 56 47 58 89 88 67   S8O....n.KVGX..g
    0020 - e4 bf 88 14 39 d7 89 bf-42 c3 e2 38 52 27 be 30   ....9...B..8R'.0
    0030 - 81 ab f2 dd 34 74 f0 88-b3 84 f9 1c 13 ad fe 87   ....4t..........
    0040 - bf 3e 6e 3a 6a 19 3a 0f-ea 1e 5e 06 72 18 15 b5   .>n:j.:...^.r...
    0050 - 3b f6 8f 0b 92 1f 2e 62-89 31 24 ec 52 e2 d8 db   ;......b.1$.R...
    0060 - bb b3 52 55 9d ed 24 e4-cd 42 47 ce 8a 41 98 16   ..RU..$..BG..A..
    0070 - de 11 a2 ae 07 3a c5 92-04 0b 25 61 8a 3a 01 60   .....:....%a.:.`
    0080 - f3 dd b0 4b ca 06 8d 58-7b 9f ce e2 10 9b a4 e4   ...K...X{.......
    0090 - fc 29 84 26 40 03 bf 5a-32 a8 bd a2 e9 3b 5a 96   .).&@..Z2....;Z.
    00a0 - 7e 63 77 3b 74 ce ed 99-c5 c3 35 0c 2b 6f 0a 01   ~cw;t.....5.+o..
    00b0 - 86 be b3 8e db 9f 44 df-c2 9f a3 5d 38 c7 09 ee   ......D....]8...
    00c0 - c0 c9 36 2d cd de dc 8d-8e 1b f5 1b 5d ea f6 04   ..6-........]...

    Start Time: 1695169985
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
bandit16@bandit:~$

C:\Users\leoga>notepad llave.txt

C:\Users\leoga>ssh -i llave.txt bandit17@bandit.labs.overthewire.org -p2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames


      ,----..            ,----,          .---.
     /   /   \         ,/   .`|         /. ./|
    /   .     :      ,`   .'  :     .--'.  ' ;
   .   /   ;.  \   ;    ;     /    /__./ \ : |
  .   ;   /  ` ; .'___,/    ,' .--'.  '   \' .
  ;   |  ; \ ; | |    :     | /___/ \ |    ' '
  |   :  | ; | ' ;    |.';  ; ;   \  \;      :
  .   |  ' ' ' : `----'  |  |  \   ;  `      |
  '   ;  \; /  |     '   :  ;   .   \    .\  ;
   \   \  ',  /      |   |  '    \   \   ' \ |
    ;   :    /       '   :  |     :   '  |--"
     \   \ .'        ;   |.'       \   \ ;
  www. `---` ver     '---' he       '---" ire.org


Welcome to OverTheWire!

If you find any problems, please report them to the #wargames channel on
discord or IRC.

--[ Playing the games ]--

  This machine might hold several wargames.
  If you are playing "somegame", then:

    * USERNAMES are somegame0, somegame1, ...
    * Most LEVELS are stored in /somegame/.
    * PASSWORDS for each level are stored in /etc/somegame_pass/.

  Write-access to homedirectories is disabled. It is advised to create a
  working directory with a hard-to-guess name in /tmp/.  You can use the
  command "mktemp -d" in order to generate a random and hard to guess
  directory in /tmp/.  Read-access to both /tmp/ is disabled and to /proc
  restricted so that users cannot snoop on eachother. Files and directories
  with easily guessable or short names will be periodically deleted! The /tmp
  directory is regularly wiped.
  Please play nice:

    * don't leave orphan processes running
    * don't leave exploit-files laying around
    * don't annoy other players
    * don't post passwords or spoilers
    * again, DONT POST SPOILERS!
      This includes writeups of your solution on your blog or website!

--[ Tips ]--

  This machine has a 64bit processor and many security-features enabled
  by default, although ASLR has been switched off.  The following
  compiler flags might be interesting:

    -m32                    compile for 32bit
    -fno-stack-protector    disable ProPolice
    -Wl,-z,norelro          disable relro

  In addition, the execstack tool can be used to flag the stack as
  executable on ELF binaries.

  Finally, network-access is limited for most levels by a local
  firewall.

--[ Tools ]--

 For your convenience we have installed a few useful tools which you can find
 in the following locations:

    * gef (https://github.com/hugsy/gef) in /opt/gef/
    * pwndbg (https://github.com/pwndbg/pwndbg) in /opt/pwndbg/
    * peda (https://github.com/longld/peda.git) in /opt/peda/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /opt/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)

 Both python2 and python3 are installed.

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us on discord or IRC.

  Enjoy your stay!

bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
bandit17@bandit:~$ exit
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| nmap | Permite realizar un escaneo a los puertos. |
## Referencias
https://overthewire.org/wargames/bandit/bandit17.html
[Port scanner on Wikipedia](https://en.wikipedia.org/wiki/Port_scanner)