----
### OBJETIVO 

---
### SOLUCION

Primero ya que en las pistas nos dicen que el archivo no abre puede ser ya que esta corrompido, asi que hay que usar un editor hexa para poder recuperar la informacion, ademas de utilizar la documentacion de los documentos para poder arreglar los datos mal puestos.
![[Pasted image 20231022234421.png]]
Una vez corregidos podemos encontrar la siguiente imagen:
![[Pasted image 20231022234630.png]]
pero no nos muestra la bandera, asi que vamos a ver los meta datos de la imagen:
![[Pasted image 20231022234727.png]]
Como podemos ver en los meta datos el archivo pesa mas de lo que deberia ya que la altura y el ancho no coinciden ya que es mas pesado de lo que deberia, dandonos a entender que la altura esta mal.  
![[Pasted image 20231022235035.png]]
Una vez que  arreglamos la altura de la imagen podemos ver la bandera:

![[Pasted image 20231022235406.png]]

picoCTF{qu1t3_a_v13w_2020}


---
### NOTAS ADICCIONALES

---
### REFERENCIAS
https://en.wikipedia.org/wiki/BMP_file_format
