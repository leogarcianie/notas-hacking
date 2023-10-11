# JaWT Scratchpad
## Objetivo
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/58210/` or http://jupiter.challenges.picoctf.org:58210
## Solución
```
JSON Web Token (JWT) es un estándar abierto basado en JSON para la creación de tokens de acceso que permiten la propagación de identidad y privilegios o claims en inglés. Por ejemplo, un servidor podría generar un token indicando que el usuario tiene privilegios de administrador y proporcionarlo a un cliente. El cliente entonces podría utilizar el token para probar que está actuando como un administrador en el cliente o en otro sistema.  El token está firmado por la clave del servidor, así que el cliente y el servidor son ambos capaces de verificar que el token es legítimo.

Después de obtener la clave, se usa para firmar un token en jwt.io, después se pega el token en el cookie editor, se recarga la página y se obtiene la flag:

picoCTF{jawt_was_just_what_you_thought_44c752f5}
```
## Notas adicionales
## Referencias