# Search source
## Objetivo
The developer of this website mistakenly left an important artifact in the website source, can you find it? The website is [here](http://saturn.picoctf.net:59405/)
## Solución
```
Para obtener la bandera de este reto, tenemos que ir la hoja de estilos del sitio web que se nos da http://saturn.picoctf.net:59405/css/style.css, y después de buscar en la gran hoja de estilos, ahi se encuentra la bandera:

 .navbar-expand-md .navbar-nav .nav-link {
     padding: 15px 48px;
     font-size: 16px;
     color: #000;
     line-height: 18px;
}
/** banner_main picoCTF{1nsp3ti0n_0f_w3bpag3s_8de925a7} **/
 .carousel-indicators li {
     width: 20px;
     height: 20px;
     border-radius: 11px;
     background-color: #070000;
}

picoCTF{1nsp3ti0n_0f_w3bpag3s_8de925a7}
```
## Notas adicionales
## Referencias