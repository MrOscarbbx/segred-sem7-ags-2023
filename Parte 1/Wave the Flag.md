
## Solucion

	┌──(kali㉿kali)-[~/Downloads]
	└─$ ls -la        
	total 24
	drwxr-xr-x  2 kali kali  4096 Sep 25 20:03 .
	drwx------ 21 kali kali  4096 Sep 25 19:56 ..
	-rw-r--r--  1 kali kali    34 Sep 25 20:01 flag
	-rw-r--r--  1 kali kali 10936 Sep 25 20:03 warm
	┌──(kali㉿kali)-[~/Downloads]
	└─$ chmod +x warm
	┌──(kali㉿kali)-[~/Downloads]
	└─$ ./warm   
	Hello user! Pass me a -h to learn what I can do!
	┌──(kali㉿kali)-[~/Downloads]
	└─$ ./warm -h
	Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}

## Notas Adicionales 
	chmod +x ...
Nos permite que un archivo binario tenga el atributo de un executable