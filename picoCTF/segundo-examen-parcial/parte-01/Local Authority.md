# Local Authority
## Objetivo
Can you get the flag? Go to this [website](http://saturn.picoctf.net:49386/) and see what you can discover.
## Solución
```
En este sitio lo que se hace es inpeccionar el sitio web, y en la parte de los sources después de fallar en el inicio de sesión se genera un archivo llamada secure.js y ahí contiene los datos correctos para ingresar al sitio y obtener la bandera:

function checkPassword(username, password)
{
	if( username === 'admin' && password === 'strongPassword098765' )
	{
		return true;
	}
	else
	{
		return false;
	}
}

Y una vez que ingresamos estos datos en el login nos da la bandera:
picoCTF{j5_15_7r4n5p4r3n7_b0c2c9cb}
```
## Notas adicionales
## Referencias