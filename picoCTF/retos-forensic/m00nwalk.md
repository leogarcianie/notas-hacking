# m00nwalk
## Objetivo
Decode this [message](https://jupiter.challenges.picoctf.org/static/14393e18d98fedbaedbc28896d7ef31a/message.wav) from the moon.
## Solución
```
Para solucionar este reto se aplicaba el método de sstv, que consiste en transmitir imagenes a traves de un canal de voz, con el siguiente comando se lee el audio y se da con una imagen que estaba ahi guardada:
sstv -d message.wav -o result.png

Y en este imagen está escrita la bandera:
picoCTF{beep_boop_im_in_space}
```
## Notas adicionales
## Referencias