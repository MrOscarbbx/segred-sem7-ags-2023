----
### OBJETIVO 
---
### SOLUCION
	┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ file buildings.png
	buildings.png: PNG image data, 657 x 438, 8-bit/color RGBA, non-interlaced
	                                                                                 
	┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ exiftool buildings.png 
	ExifTool Version Number         : 12.57
	File Name                       : buildings.png
	Directory                       : .
	File Size                       : 625 kB
	File Modification Date/Time     : 2020:10:26 14:30:20-04:00
	File Access Date/Time           : 2023:10:16 01:45:23-04:00
	File Inode Change Date/Time     : 2023:10:16 01:45:15-04:00
	File Permissions                : -rw-r--r--
	File Type                       : PNG
	File Type Extension             : png
	MIME Type                       : image/png
	Image Width                     : 657
	Image Height                    : 438
	Bit Depth                       : 8
	Color Type                      : RGB with Alpha
	Compression                     : Deflate/Inflate
	Filter                          : Adaptive
	Interlace                       : Noninterlaced
	Image Size                      : 657x438
	Megapixels                      : 0.288
	                                                                                 
	┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ open buildings.png                                                                                                                        
	┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ sudo gem install zsteg                          
	Fetching iostruct-0.0.5.gem
	Fetching rainbow-3.1.1.gem
	Fetching zsteg-0.2.13.gem
	Fetching zpng-0.4.5.gem
	Successfully installed rainbow-3.1.1
	Successfully installed zpng-0.4.5
	Successfully installed iostruct-0.0.5
	Successfully installed zsteg-0.2.13
	Parsing documentation for rainbow-3.1.1
	Installing ri documentation for rainbow-3.1.1
	Parsing documentation for zpng-0.4.5
	Installing ri documentation for zpng-0.4.5
	Parsing documentation for iostruct-0.0.5
	Installing ri documentation for iostruct-0.0.5
	Parsing documentation for zsteg-0.2.13
	Installing ri documentation for zsteg-0.2.13
	Done installing documentation for rainbow, zpng, iostruct, zsteg after 6 seconds
	4 gems installed
	                                                                                 
	┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ zsteg -a buildings.png | grep pico
	b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"

---
### NOTAS ADICCIONALES
La esteganografía es una **técnica de cifrado alternativa que oculta un mensaje secreto, encerrándolo en un archivo ordinario, como un archivo gráfico de película o de sonido**. El cifrado oculta el contenido de la información, pero no intenta disfrazar el hecho de que la información existe

---
### REFERENCIAS
https://es.linkedin.com/learning/recursos-de-arquitectura-y-diseno-seguros-comptia-security-plus-sy0-601/que-es-la-esteganografia#:~:text=La%20esteganograf%C3%ADa%20es%20una%20t%C3%A9cnica,de%20que%20la%20informaci%C3%B3n%20existe.