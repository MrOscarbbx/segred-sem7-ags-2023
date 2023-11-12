## Solucion
	┌──(kali㉿kali)-[~/Downloads]
	└─$ nc saturn.picoctf.net 49700
	'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
	┌──(kali㉿kali)-[~/Downloads]
	└─$ python          
	Python 3.11.2 (main, Mar 13 2023, 12:18:29) [GCC 12.2.0] on linux
	Type "help", "copyright", "credits" or "license" for more information.
	print('picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}')
	picoCTF{gl17ch_m3_n07_a4392d2e}
	 	listo jijij

Para esta solucion utilice Python ya que se esta utilizando la funcion "chr" que es correspondiente a python.