# Forbidden Paths
## Objetivo
Can you get the flag? Here's the [website](http://saturn.picoctf.net:64403/). We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?
## Solución
```
En la descripción de este reto se nos indíca que nos encontramos en /usr/share/nginx/html/ y como vamos a acceder a la ruta /flag.txt realizamos una carga de recorrido de directorios, con ../../../../flag.txt, y ahi obtenemos la bandera:

picoCTF{7h3_p47h_70_5ucc355_e5fe3d4d}
```
## Notas adicionales
## Referencias