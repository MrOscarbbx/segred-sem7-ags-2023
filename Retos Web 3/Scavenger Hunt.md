## Solucion
Como en un ejercicio anterior empezamos buscando en el HTML por algun comentario:
![[Pasted image 20231011172846.png]]
<!-- Here's the first part of the flag: picoCTF{t -->
Y encontramos la primera parte
Ahora buscamos en el css:
![[Pasted image 20231011172932.png]]
Y encontramos la segunda parte de la bander
/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 *
Ahora buscamos en JS :
![[Pasted image 20231011173303.png]]
Vemos un comentario que es una pregunta, al buscarlo en google nos muestra que la respuesta es robots.txt que ya habiamos utilizado en un reto anterior
![[Pasted image 20231011173254.png]]
Entramos a el archivo robots.txt
![[Pasted image 20231011173341.png]]
Encontramos la tercera parte y una pregunta 
	# Part 3: t_0f_pl4c
La pregunta hace referencia a un archivo de apache que normalmente esta oculto que es el .htaccess, asi que entramos a el htacces 
![[Pasted image 20231011173629.png]]
Encontramos la parte cuatro de la bandera y una referencia a MAC
	# Part 4: 3s_2_lO0k
Asi que vamos a buscar un archivo que esta oculto normalmente en mac que es el DS_Store
![[Pasted image 20231011173820.png]]
y asi encontramos la ultima parte de la bandera.
Congrats! You completed the scavenger hunt. Part 5: _7a46d25d}


## Notas Adicionales
El archivo **htaccess** (acceso de hipertexto) es un archivo oculto que se utiliza para configurar funciones adicionales para sitios web alojados en el servidor web Apache. Con él, puedes reescribir la URL, proteger directorios con contraseña, habilitar la protección de enlaces directos, no permitir el acceso a direcciones IP específicas, cambiar la zona horaria de tu sitio web o alterar la página de índice predeterminada, y mucho más. Aquí aprenderás a localizar y crear archivos **.htaccess**.

En el sistema operativo macOS de Apple, .DS_Store es un archivo que almacena atributos personalizados de la carpeta que lo contiene, como la posición de los iconos o la imagen de fondo.1​ El nombre es una abreviación de desktop services store2​ (‘almacén de servicios de escritorio’), el cual denota su propósito; sus funciones se asemejan a las del archivo desktop.ini de Microsoft Windows. El programa Finder crea y actualiza un archivo .DS_Store para cada una de las carpetas. Al comenzar con un carácter de punto, su nombre permite ocultar el archivo de manera predeterminada en Finder y otras herramientas de Unix. Su estructura interna es privativa.3​
## Referencias
https://www.hostinger.mx/tutoriales/que-es-el-archivo-htaccess
https://es.wikipedia.org/wiki/.DS_Store