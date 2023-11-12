
 Entramos a la pagina con el netcat:
 
	 ┌──(kali㉿kali)-[~/Downloads]
	└─$ nc jupiter.challenges.picoctf.org 7480            
	This is defintely not a flag
	Again, I really don't think this is a flag
	Again, I really don't think this is a flag
	This is defintely not a flag
	Again, I really don't think this is a flag
	I don't think this is a flag either
	Again, I really don't think this is a flag
	This is defintely not a flag
	.......
Y nos sale un monton de lineas asi que vamos a usar nuestro magico grep

	┌──(kali㉿kali)-[~/Downloads]
	└─$ nc jupiter.challenges.picoctf.org 7480 | grep pico
	picoCTF{digital_plumb3r_06e9d954}

y listo.