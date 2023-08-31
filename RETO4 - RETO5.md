----
### OBJETIVO 
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

---
### DATOS DE ACCESO
	Servidor : ssh bandit3@bandit.labs.overthewire.org -p 2220 
	Contraseña : 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe 

---
### SOLUCION
	bandit4@bandit:~/inhere$ cd ..
	bandit4@bandit:~$ cd inhere/
	bandit4@bandit:~/inhere$ ls
		-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
	bandit4@bandit:~/inhere$ file ./*
		./-file00: data
		./-file01: data
		./-file02: data
		./-file03: data
		./-file04: data
		./-file05: data
		./-file06: data
		./-file07: ASCII text
		./-file08: data
		./-file09: Non-ISO extended-ASCII text, with no line terminators
	bandit4@bandit:~/inhere$ cat ./-file07
	Contraseña : lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

---
### NOTAS ADICCIONALES

En casos como este en el que se tiene que encontrar un tipo especifico de documento entre varios se puede utilizar el comando file para poder saber que tipo de archivo son, además de que gracias a el comodín "`*`" podemos ver cual es el tipo de archivo de cada uno de los archivos que se encuentran en el directorio.  

---
### REFERENCIAS
