## Solución
Iniciamos corriendo el programa

	┌──(kali㉿kali)-[~/Downloads]
	└─$ python level2.py                    
	Please enter correct password for flag: 

Nos piden una contraseña pero no nos dan ninguna pista así que vamos a ver el código otra ves:
![[Pasted image 20230927000644.png]]
Y párese ser que en la verificación ya nos dicen cual es la contraseña pero esta en código 
así que al igual que en un reto anterior, podemos usar python para poder decodificar esto

	 ┌──(kali㉿kali)-[~/Downloads]
	└─$ python 
	Python 3.11.2 (main, Mar 13 2023, 12:18:29) [GCC 12.2.0] on linux
	Type "help", "copyright", "credits" or "license" for more information.
	print(chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39))
	4ec9
Ahora solo ponemos la contraseña en el input

	┌──(kali㉿kali)-[~/Downloads]
	└─$ python level2.py
	Please enter correct password for flag: 4ec9
	Welcome back... your flag, user:
	picoCTF{tr45h_51ng1ng_9701e681}

Y listo :)