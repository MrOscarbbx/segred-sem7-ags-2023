----
### OBJETIVO 
Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.

---
### SOLUCION
El Archivo que descarga en el reto, es un audio y nos dan una pista que nos pregunta como es que se mandaron las primeras imagenes de la luna a la tierra, e investigando podemos encontrar que el formato en el que se decodificaron los audios mandados desde la luna fueron en sstv, entonces procedemos a descargar un decodificador de sstv

	 ┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ sstv -d message.wav -o moon.png
	[sstv] Searching for calibration header... Found!    
	[sstv] Detected SSTV mode Scottie 1
	[sstv] Decoding image...   [###############################################] 100%
	[sstv] Drawing image data...
	[sstv] ...Done!
	                                                                                 
	┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ open moon.png     
	
![[moon.png]]

picoCTF{beep_boop_im_in_space}

---
### NOTAS ADICCIONALES

Decodificador de sstv:
## [Installation](https://github.com/colaclanth/sstv#installation)

```
$ git clone https://github.com/colaclanth/sstv.git

$ python setup.py install
```

## [Usage](https://github.com/colaclanth/sstv#usage)

```
$ sstv -d audio_file.wav -o result.png
```

---
### REFERENCIAS
https://github.com/colaclanth/sstv