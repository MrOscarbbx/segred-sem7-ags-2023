----
### OBJETIVO 

---
### SOLUCION
	┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ ls
	capture.pcap  flag.txt  garden  pico_img.png
	                                                                                 
	┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ file flag.txt    
	flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced
	                                                                                 
	┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ mv flag.txt flag.png
	                                                                                 
	┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ open flag.png 

![[flag.png]]
En este problema solo regresamos el archivo a su extencion original

---
### NOTAS ADICCIONALES

---
### REFERENCIAS
