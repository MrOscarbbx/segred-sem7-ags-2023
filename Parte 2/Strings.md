## Solucion
	┌──(kali㉿kali)-[~/Downloads]
	└─$ file strings 
	strings: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=047a5079a5f563cd0e540d28f42a37161093ffda, not stripped
	┌──(kali㉿kali)-[~/Downloads]
	└─$ strings strings | grep pico     
	picoCTF{5tRIng5_1T_827aee91}

Aqui el nombre de el reto me ayudo ya que dice literal la herramienta que se va a utilizar, y teniendo eso en cuenta solo era usar un clasico grep y vamonos