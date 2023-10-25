----
### OBJETIVO 
This [garden](https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg) contains more than it seems.

---
### SOLUCION
	┌──(kali㉿kali)-[~/Picoctf/forense/garden]
	└─$ ls 
	garden.jpg
	                                                                                 
	┌──(kali㉿kali)-[~/Picoctf/forense/garden]
	└─$ file garden.jpg 
	garden.jpg: JPEG image data, JFIF standard 1.01, resolution (DPI), density 72x72, segment length 16, baseline, precision 8, 2999x2249, components 3
	┌──(kali㉿kali)-[~/Picoctf/forense/garden]
	└─$ strings garden.jpg | grep pico
	Here is a flag "picoCTF{more_than_m33ts_the_3y3657BaB2C}"

---
### NOTAS ADICCIONALES
Tambien se puede utilizar un editor hexa, como hexeditor en kali

---
### REFERENCIAS
