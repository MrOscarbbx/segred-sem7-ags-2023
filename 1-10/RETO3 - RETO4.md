----
### OBJETIVO
The password for the next level is stored in a hidden file in the **inhere** directory.

---
### DATOS DE ACCESO
	Servidor : ssh bandit3@bandit.labs.overthewire.org -p 2220
	Contraseña : aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

---
### SOLUCION
	bandit3@bandit:~$ ls
		inhere
	bandit3@bandit:~$ ls -la inhere/
		total 12
		drwxr-xr-x 2 root    root    4096 Apr 23 18:04 .
		drwxr-xr-x 3 root    root    4096 Apr 23 18:04 ..
		-rw-r----- 1 bandit4 bandit3   33 Apr 23 18:04 .hidden
	bandit3@bandit:~$ cat inhere/.hidden
	Contraseña : 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

---
### NOTAS ADICCIONALES
Existen archivos ocultos los cuales solo puedes ver si en el comando "ls" utilizas las opciones "-a" para poder ver los archivos ocultos.
Y al momento de ver el archivo puedes leerlo con cat solo poniendo la path relativa.

---
### REFERENCIAS
