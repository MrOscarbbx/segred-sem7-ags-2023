----
### OBJETIVO
The password for the next level is stored in a file called **-** located in the home directory

---
### DATOS DE ACCESO
	Servidor: ssh bandit1@bandit.labs.overthewire.org -p 2220
	Contraseña: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

---
### SOLUCION
	ssh bandit1@bandit.labs.overthewire.org -p 2220
	bandit1@bandit:~$ ls
	-
	bandit1@bandit:~$ cat ./-
	Contraseña : rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

---
### NOTAS ADICCIONALES

El carácter especial "-" ( guion ) , cuando están al principio del nombre de algún archivo, necesita que ser llamado con una path relativa o absoluta para evitar confusiones. 

### REFERENCIAS
