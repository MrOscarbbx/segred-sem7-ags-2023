## Solucion
Primero corri el programa para ver que es lo que estaba mal:
	
	┌──(kali㉿kali)-[~/Downloads]
	└─$ python fixme1.py   
	  File "/home/kali/Downloads/fixme1.py", line 20
	    print('That is correct! Here\'s your flag: ' + flag)
	IndentationError: unexpected indent
Podemos ver que es una indentacion incorrecta
Asi que abrimos el vscode para arreglarlo porque aun no se salirme de nano ni de vi

	┌──(kali㉿kali)-[~/Downloads]
	└─$ code fixme1.py  	

 ![[Pasted image 20230925215845.png]]
Guardamos y corremos otra vez:

	┌──(kali㉿kali)-[~/Downloads]
	└─$ python fixme1.py
	That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}

Y listo! :)