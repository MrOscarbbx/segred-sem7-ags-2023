----
### OBJETIVO
The password for the next level is stored in a file called **spaces in this filename** located in the home directory

---
### DATOS DE ACCESO
	Servidor : ssh bandit2@bandit.labs.overthewire.org -p 2220
	Contraseña : rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

---
### SOLUCION
	ssh bandit3@bandit.labs.overthewire.org -p 2220
	bandit2@bandit:~$ ls
	spaces in this filename
	bandit2@bandit:~$ cat "spaces in this filename"
	Contraseña : aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

---
### NOTAS ADICCIONALES

Los nombre de archivos que tienen un espacio, es necesario que se pongan entre comillas para que el nombre se lea de manera correcta y que si no se tomara como diferentes archivos.  

---
### REFERENCIAS
