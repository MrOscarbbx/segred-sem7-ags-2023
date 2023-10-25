----
### OBJETIVO 
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

---
### DATOS DE ACCESO
	Servidor : ssh -i llave.txt bandit17@localhost -p 2220
	Llave : llave.txt
	Contraseña : VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e

---
### SOLUCION
	bandit17@bandit:~$ ls
		passwords.new  passwords.old
	bandit17@bandit:~$ diff passwords.old passwords.new --color
		42c42
	<glZreTEH1V3cGKL6g4conYqZqaEj0mte
	>Contraseña : hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
	

---
### NOTAS ADICCIONALES
El comando diff, como lo podemos suponer por el nombre nos muestra las diferencias entre dos archivos linea por linea, en este caso solo nos muestra la contraseña pero en un archivo con mas cambio nos mostraria todas las diferencias

---
### REFERENCIAS
