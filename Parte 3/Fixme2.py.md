
## Solucion

Primero corremos el programa para poder ver que es lo que esta mal:

	┌──(kali㉿kali)-[~/Downloads]
	└─$ python fixme2.py
	  File "/home/kali/Downloads/fixme2.py", line 22
	    if flag = "":
	       ^^^^^^^^^
	SyntaxError: invalid syntax. Maybe you meant ' == ' or ':=' instead of '=' 
Una ves que sabemos que esta mal vamos a buscarlo
Abrimos el codigo en un editor para arreglar el problema

	┌──(kali㉿kali)-[~/Downloads]
	└─$ code fixme2.py

![[Pasted image 20230926234249.png]]
Una ves corregimos los errores volvemos a correr el programa para poder conseguir la bandera 

	 ┌──(kali㉿kali)-[~/Downloads]
	└─$ python fixme2.py
	That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}

Y listo, ya todo estaria terminado.