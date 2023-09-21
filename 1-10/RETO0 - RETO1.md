----
### OBJETIVO 
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

----
### DATOS DE ACCESO
	Contraseña : bandit0

---
### SOLUCION
	ssh bandit0@bandit.labs.overthewire.org -p 2220
	bandit0@bandit:~$ ls
	readme
	bandit0@bandit:~$ cat readme
	contraseña : NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

---
### NOTAS ADICCIONALES
	Los archivos tipo Ascii text Se pueden abrir desde la linea de comandos con el comando "cat"
### REFERENCIAS
