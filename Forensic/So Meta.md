----
### OBJETIVO 

---
### SOLUCION	                                                                                 
	┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ exiftool pico_img.png 
	ExifTool Version Number         : 12.57
	File Name                       : pico_img.png
	Directory                       : .
	File Size                       : 109 kB
	File Modification Date/Time     : 2020:10:26 14:38:23-04:00
	File Access Date/Time           : 2023:10:16 00:49:35-04:00
	File Inode Change Date/Time     : 2023:10:16 00:49:18-04:00
	File Permissions                : -rw-r--r--
	File Type                       : PNG
	File Type Extension             : png
	MIME Type                       : image/png
	Image Width                     : 600
	Image Height                    : 600
	Bit Depth                       : 8
	Color Type                      : RGB
	Compression                     : Deflate/Inflate
	Filter                          : Adaptive
	Interlace                       : Noninterlaced
	Software                        : Adobe ImageReady
	XMP Toolkit                     : Adobe XMP Core 5.3-c011 66.145661, 2012/02/06-14:56:27
	Creator Tool                    : Adobe Photoshop CS6 (Windows)
	Instance ID                     : xmp.iid:A5566E73B2B811E8BC7F9A4303DF1F9B
	Document ID                     : xmp.did:A5566E74B2B811E8BC7F9A4303DF1F9B
	Derived From Instance ID        : xmp.iid:A5566E71B2B811E8BC7F9A4303DF1F9B
	Derived From Document ID        : xmp.did:A5566E72B2B811E8BC7F9A4303DF1F9B
	Warning                         : [minor] Text/EXIF chunk(s) found after PNG IDAT (may be ignored by some readers)
	Artist                          : picoCTF{s0_m3ta_fec06741}
	Image Size                      : 600x600
	Megapixels                      : 0.360

---
### NOTAS ADICCIONALES
La definición más concreta de los metadatos es qué son “**datos acerca de los datos**” y sirven para suministrar información sobre los datos producidos. Los metadatos consisten en información que caracteriza datos, describen el contenido, calidad, condiciones, historia, disponibilidad y otras características de los datos.
ExifTool es un programa de software gratuito y de código abierto para leer, escribir y manipular metadatos de imágenes, audio, vídeo y PDF. Es independiente de la plataforma y está disponible como biblioteca Perl y como aplicación de línea de comandos.

---
### REFERENCIAS
https://www.geoidep.gob.pe/catalogo-metadatos/que-son-los-metadatos#:~:text=La%20definici%C3%B3n%20m%C3%A1s%20concreta%20de,otras%20caracter%C3%ADsticas%20de%20los%20datos.

https://en.wikipedia.org/wiki/ExifTool