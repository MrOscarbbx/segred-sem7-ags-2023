
## Solucion
	┌──(kali㉿kali)-[~/Downloads]
	└─$ nc mercury.picoctf.net 43239                             
	112 
	105 
	99 
	111 
	67 
	84 
	70 
	123 
	103 
	48 
	48 
	100 
	95 
	107 
	49 
	116 
	116 
	121 
	33 
	95 
	110 
	49 
	99 
	51 
	95 
	107 
	49 
	116 
	116 
	121 
	33 
	95 
	55 
	99 
	48 
	56 
	50 
	49 
	102 
	53 
	125 
	10 
	                                                                                                                                                                       
	┌──(kali㉿kali)-[~/Downloads]
	└─$ nc mercury.picoctf.net 43239 | awk '{ printf "%c", $1 }';
	picoCTF{g00d_k1tty!_n1c3_k1tty!_7c0821f5}

## Notas Adicionales
Los usos básicos que podemos dar al comando Awk son los siguientes:

1. Buscar palabras y patrones de palabras y reemplazarlos por otras palabras y/o patrones.
2. Hacer operaciones matemáticas.
3. Procesar texto y mostrar las líneas y columnas que cumplen con determinadas condiciones.
4. Etc.

|**conversion character**|**argument type**|
|---|---|
|**d**, **i**|An integer, expressed as a decimal number.|
|**o**|An integer, expressed as an unsigned [octal](https://www.computerhope.com/jargon/o/octal.htm) number.|
|**x**, **X**|An integer, expressed as an unsigned [hexadecimal](https://www.computerhope.com/jargon/h/hex.htm) number|
|**u**|An integer, expressed as an unsigned decimal number.|
|**c**|An integer, expressed as a character. The integer corresponds to the character's [ASCII code](https://www.computerhope.com/jargon/a/ascii.htm).|
|**s**|A string.|

## Referencias
https://geekland.eu/uso-del-comando-awk-en-linux-y-unix-con-ejemplos/
