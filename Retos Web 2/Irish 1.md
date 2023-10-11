## Solución
Primero vamos a entrar a a pagina para poder ver que estamos apunto de hackear
![[Pasted image 20231004103352.png]]
Vemos que tenemos un login así que intentamos entrar
![[Pasted image 20231004103409.png]]
No podemos entrar porque no tenemos tanta suerte asi que inspeccionamos la pagina para encontrar debilidades en el cliente
![[Pasted image 20231004103454.png]]
Al entrar al cliente encontramos una opción que esta oculta que nos muestra como es que se mandan a llamar las consultas en el php
![[Pasted image 20231004104434.png]]
Procedemos a inyectar una consulta para poder entrar a la pagina sin tener la contraseña
![[Pasted image 20231004104513.png]]

## Notas Adicionales 
La inyección SQL es un tipo de ciberataque web que **consiste en ejecutar comandos en lenguaje SQL, para leer, modificar, añadir o eliminar información de una base de datos de una aplicación**. Estos ciberataques suelen ocurrir debido a una falta de validación de los inputs de los usuarios.****