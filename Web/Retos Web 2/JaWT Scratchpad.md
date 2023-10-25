## Solucion 
Entramos a la pagina para ver que rollo con lo que tnenemos
![[Pasted image 20231009174641.png]]
Al momento de logearnos con cualquier nombre nos produce una cookie en jwt
![[Pasted image 20231010001802.png]]
esta nos va a servir para poder obtener la contraseña del admin asi que tenemos que sacar entre el token la contraseña, para eso usamos la herramienta john, asi que primero metemos el token en un archivo
![[Screenshot_2023-10-10_01_35_56.png]]
para despues usar la herramienta john para poder sacar la contraseña del token
![[Screenshot_2023-10-10_01_42_03.png]]
una ves sacando la contraseña usando jwt podemos decodificar el token y modificarlo para poder entar como el admin
![[Screenshot_2023-10-10_01_42_29.png]]
Asi que cambiamos el user por "admin" y la contraseña por ilovepico
![[Screenshot_2023-10-10_01_43_23.png]]
ya solo editamos la cookie y recargamos para que la pagina tome el token y nos haga como log como admin y listo
![[Pasted image 20231010000959.png]]