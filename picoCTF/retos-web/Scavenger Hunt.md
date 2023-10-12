# Scavenger Hunt
## Objetivo
There is some interesting information hidden around this site [http://mercury.picoctf.net:39491/](http://mercury.picoctf.net:39491/). Can you find it?
## Solución
```
El flag de este reto se encontrba en el código fuente del sitio:

<!-- Here's the first part of the flag: picoCTF{t -->
/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */
# Part 3: t_0f_pl4c
# Part 4: 3s_2_lO0k
Congrats! You completed the scavenger hunt. Part 5: _f7ce8828}

Las distintas partes se encontraban en el CSS, robots.txt, htaccess y DS_Store:

picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_f7ce8828}
```
## Notas adicionales
## Referencias