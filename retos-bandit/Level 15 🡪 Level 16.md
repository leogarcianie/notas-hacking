# Level 15 🡪 Level 16
## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.
## Datos de acceso al nivel
```
Server: bandit.labs.overthewire.org
User: bandit15
Password: jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```
## Solución
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Sep  9 01:47:01 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Sep  9 01:47:01 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Sep  9 01:46:01 2023 GMT; NotAfter: Sep  9 01:47:01 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEC3lb1TANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwOTA5MDE0NjAxWhcNMjMwOTA5MDE0NzAxWjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDE
6JvfXGuRLl9vhsp6vfdk+yRxsWQlE5vKo8PoOxofsNPdmOH2H5loItC0kRCLyZj5
Byaeg/T4RWDgmLdBLUqSsMTZoUAFKBepLFjYqULJ+fduZSntt2Z6YqZJTHWJ/zzX
ib5i9jktlX/FJxJFO6/ypjbEZX34QHrlZ2MQv2C7bHiccVUf1PlSbDHgTZ4kq8Hy
g6S7YpsC/ddwowzjVV10b0hqqw9XJEHesvKZYDyblnJdTLbiFbWI921el1WaQavu
/jsKT6AGZpgH3ouK7FSLCKO8fF0wA3/H+8CWoLyjuK4S130gKzpanQQ+RXVwcMyJ
6CdfNVCH4MCJ398ZnVi/AgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCZ
AD6KmVr+auzrS6J5rA6i+tCNsCJnTJVfZHETouLgd9iFd8TvJCPaTxI8w91Zuk8b
kUpfW7ZRhkYP3K8w4iqogg+73DHVCVhMd1zGRL//HF3IKtmNrEv0nNSrrscEgepS
m/XGyFsmgXzUTmZ/0eghVGE7fMHRbO8e9ITjqlvRMcZN4ycm1o0KTfc0Awem7dro
oF6a+La5KLsuexubxO6y+uf87seLwWcR6WagszJSJPCCpCnCjEXzAPqu0nXfLBlY
IjA8qJh5ZTeL4CVxWNilpZ/bZWv9V74FsVCDHnhE+DRB1ZflEPar+nqT7AncnVbN
FJSTxHOxfdwiZ/xygyem
-----END CERTIFICATE-----
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit15@bandit:~$
```
## Notas adicionales
| Comando | Descripción |
|------------------|----------------|
| openssl s_client | Conectamos a un host en un puerto especifico, encontrándome en un canal seguro para comunicarse. |
## Referencias
https://overthewire.org/wargames/bandit/bandit16.html
[Secure Socket Layer/Transport Layer Security on Wikipedia](https://en.wikipedia.org/wiki/Secure_Socket_Layer)
[OpenSSL Cookbook - Testing with OpenSSL](https://www.feistyduck.com/library/openssl-cookbook/online/ch-testing-with-openssl.html)