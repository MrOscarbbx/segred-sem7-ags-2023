----
### OBJETIVO 
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

---
### DATOS DE ACCESO
	Servidor : ssh bandit11@bandit.labs.overthewire.org -p 2220
	Contraseña : 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

---
### SOLUCION
	bandit11@bandit:~$ ls
		data.txt
	bandit11@bandit:~$ cat data.txt
		Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
	bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
		The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
---
### NOTAS ADICCIONALES
El **`tr`** comando es una utilidad de línea de comandos de Linux que traduce o elimina caracteres de la entrada estándar ( **`stdin`**) y escribe el resultado en la salida estándar ( **`stdout`**). Úselo **`tr`** para realizar diferentes transformaciones de texto, incluida la conversión de mayúsculas y minúsculas, comprimir o eliminar caracteres y reemplazo básico de texto.

La sintaxis basica es:

	tr [options] SET1 [SET2]

Ejemplo: 

	bandit11@bandit:~$ echo "Hello World" | tr l M
		HeMMo WorMd

Lo que hicimos fue modificar el inicio del abecedario de A hacia M que son 13 letras mas adelante 

---
### REFERENCIAS
https://phoenixnap.com/kb/linux-tr#:~:text=The%20tr%20command%20is%20a,characters%2C%20and%20basic%20text%20replacement.