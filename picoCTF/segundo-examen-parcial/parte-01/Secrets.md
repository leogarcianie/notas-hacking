# Secrets
## Objetivo
We have several pages hidden. Can you find the one with the flag? The website is running [here](http://saturn.picoctf.net:62050/).
## Solución
```
Para obtener la bandera de este reto, me dí cuenta que hay una carpeta en los sources llamada secret, y haciendo pruebas guiandome por la pista del reto, fui por más carpetas y ahí en la ruta: http://saturn.picoctf.net:62050/secret/hidden/superhidden/ se encontraba un sitio, y solo viendo el código fuente ahi estaba la bandera:

<!DOCTYPE html>
<html>
	<head>
		<title></title>
		<link rel="stylesheet" href="[mycss.css](http://saturn.picoctf.net:62050/secret/hidden/superhidden/mycss.css)" />
	</head>
	<body>
		<h1>Finally. You found me. But can you see me</h1>
		<h3 class="flag">picoCTF{succ3ss_@h3n1c@10n_51b260fe}</h3>
	</body>
</html>

picoCTF{succ3ss_@h3n1c@10n_51b260fe}
```
## Notas adicionales
## Referencias