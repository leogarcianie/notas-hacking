# GET aHEAD
## Objetivo
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:47967/](http://mercury.picoctf.net:47967/)
## Solución
```
Aquí utilicé Burp Suite para interceptar la solicitud del botón "Choose Blue", cambiando la solicitud de POST al método HEAD, y después de esto el historial del proxy en Burp Suite nos devuelve la flag:

picoCTF{r3j3ct_th3_du4l1ty_cca66bd3}
```
## Notas adicionales
## Referencias