----
### OBJETIVO 
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

---
### DATOS DE ACCESO
	Servidor : ssh bandit10@bandit.labs.overthewire.org -p 2220
	Contraseña : G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

---
### SOLUCION
	bandit10@bandit:~$ ls
		data.txt
	bandit10@bandit:~$ cat data.txt
		VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
	bandit10@bandit:~$ cat data.txt | base64 -d
		The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

---
### NOTAS ADICCIONALES
Para codificar o decodificar entradas/salidas estándar o cualquier contenido de archivo, Linux utiliza un sistema de codificación y decodificación base64. Los datos se codifican y decodifican para facilitar el proceso de transmisión y almacenamiento de datos.

## BASE64
| Opcion | Accion |
|-|-|
|**-e or –encode**| This option is used to encode any data from standard input or from any file. It is the default option.
|**-d or –decode**| This option is used to decode any encoded data from standard input or from any file.
|**-n or –noerrcheck**|  By default, base64 checks error while decoding any data. You can use –n or –noerrcheck option to ignore checking at the time of decoding.
|**-u or –help**| This option is used to get information about the usage of this command.
|**-i, –ignore-garbage**|  This option is used to ignore non-alphabet character while decoding.

---
### REFERENCIAS
https://linuxhint.com/bash_base64_encode_decode/