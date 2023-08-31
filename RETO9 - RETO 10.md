----
### OBJETIVO 
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

---
### DATOS DE ACCESO
	Servidor : ssh bandit9@bandit.labs.overthewire.org -p 2220
	Contraseña : EN632PlfYiZbn3PhVK3XOGSlNInNE00t

---
### SOLUCION
	bandit9@bandit:~$ ls
		data.txt
	bandit9@bandit:~$ wc data.txt
		   79   451 19379 data.txt
	bandit9@bandit:~$ strings data.txt | grep ==
		4========== the#
		========== password
		========== is
		========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
	Contraseña : G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

---
### NOTAS ADICCIONALES
El comando Strings sirve para poder filtrar las cadenas que se pueden mostrar como cadena y no como un tipo de bytes
***The **strings** command looks for printable strings in a file. A string is any sequence of 4 or more printable characters that end with a new-line or a null character. The **strings** command is useful for identifying random object files.***

---
### REFERENCIAS
https://www.ibm.com/docs/en/aix/7.2?topic=s-strings-command