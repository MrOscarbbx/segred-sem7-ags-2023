## Solucion
Entramos a la pagina y entramos a ver las cookies:
![[Pasted image 20231011105341.png]]
Al cambiar a la cookie de -1 a 1 nos muestra esto asi que tenemos que encontrar el numero adecuado para poder encontrar la bandera
![[Pasted image 20231011175326.png]]
Despues de varios intentos podemos encontrar la bandera en el numero 18
![[Pasted image 20231011175518.png]]
Tambien podemos utilizar un for y un curl para poder encontrar la bandera de maner mas sencilla:

``` bash
	mrioso-picoctf@webshell:~$ for i in {1..20}; do curl -s http://mercury.picoctf.net:17781/check -H "Cookie: name=$i"; done | grep pico
	<p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_bb3b3535}</code></p>
```
	            
De hecho hay otras maneras pero creo que estas son las mas faciles