# Roboto Sans
## Objetivo
The flag is somewhere on this web application not necessarily on the website. Find it. Check [this](http://saturn.picoctf.net:63195/) out.
## Solución
```
Para obtener la bandera de este reto primero vamos al archivo robots.txt donde se encuentra la siguiente:

User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/

Esto me indíca que hay algo encriptado, en este caso en base64, y encontramos que la segunda línea nos da la ruta js/myfile.txt, y ahi vamos a esa ruta, y aquí se encuentra la bandera<.
http://saturn.picoctf.net:63195/js/myfile.txt

picoCTF{Who_D03sN7_L1k5_90B0T5_22ce1f22}
```
## Notas adicionales
## Referencias