# Includes
## Objetivo
Can you get the flag? Go to this [website](http://saturn.picoctf.net:61941/) and see what you can discover.
## Solución
```
La bandera de este reto se obtuvo por medio de un sitio web, la primera parte de la bandera estaba en la hoja de estilos css http://saturn.picoctf.net:61941/style.css:

body {
  background-color: lightblue;
}

/*  picoCTF{1nclu51v17y_1of2_  */

La segunda parte de la bandera se obtuvo en el archivo de javascript del mismo sitio http://saturn.picoctf.net:61941/script.js:

function greetings()
{
  alert("This code is in a separate file!");
}

//  f7w_2of2_6edef411}


picoCTF{1nclu51v17y_1of2_f7w_2of2_6edef411}
```
## Notas adicionales
## Referencias