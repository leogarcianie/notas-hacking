# shark on wire 1
## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
## Solución
```
Se nos da un archivo de paquetes, en este caso se descarga el archivo en kali linux, y se abre con la herramienta 'WireShark', y de ahi se sigue el stream del primer paquete UDP con 'Follow' y 'UDP Stream', se busca en los diferentes streams, y ahi se encuentra la bandera en el stream 6:

picoCTF{StaT31355_636f6e6e}
```
## Notas adicionales
## Referencias