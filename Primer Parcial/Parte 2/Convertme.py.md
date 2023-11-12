## Solucion:
	┌──(kali㉿kali)-[~/Downloads]
	└─$ python convertme.py 
	If 58 is in decimal base, what is it in binary base?
	Answer: 111010
	That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}

	┌──(kali㉿kali)-[~]
	└─$ echo "ibase=10;obase=2;58" | bc        
	111010

Utilice el codigo del ejercicio anterior para convertir el numero