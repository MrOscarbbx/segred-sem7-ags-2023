----
### OBJETIVO 
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.

---
### DATOS DE ACCESO
	Servidor : ssh bandit25@bandit.labs.overthewire.org -p 2220
	Contraseña : p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d

---
### SOLUCION

Se debe de usar una debilidad del lector de texto more, haciendo mas pequeña la consola para que no salga todo el texto de inicio dandonos oportunidad de entrar como el usuario bandit26

![[Pasted image 20230920212456.png]]
![[Pasted image 20230920212539.png]]
![[Pasted image 20230920212411.png]]


---
### NOTAS ADICCIONALES
El comando more te permite mostrar el resultado de la ejecución de un comando en la terminal de a una página a la vez. Esto es especialmente útil cuando se ejecuta un comando que causa un gran desplazamiento, como el **comando ls** o el **comando du**.

---
### REFERENCIAS
https://www.neoguias.com/comando-more-linux/#Que_hace_el_comando_more_de_Linux