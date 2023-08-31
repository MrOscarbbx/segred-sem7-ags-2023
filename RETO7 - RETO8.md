----
### OBJETIVO 
The password for the next level is stored in the file **data.txt** next to the word **millionth**

---
### DATOS DE ACCESO
	Servidor : ssh bandit7@bandit.labs.overthewire.org -p 2220
	Contraseña : z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

---
### SOLUCION
	bandit7@bandit:~$ ls
		data.txt
	bandit7@bandit:~$ cat data.txt | grep millionth
		millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
	Contraseña : TESKZC0XvTetK0S9xNwm25STk5iWrBvP
---
### NOTAS ADICCIONALES

El Comando Grep es un esencial a la hora de filtrar datos por strings, para su uso se puede usar en especifico en un documento de la siguiente manera:

	grep "string" file

O también usando el "|" (pipe) que es un carácter que toma la salida de un comando de la izquierda y lo pasa como entrada al comando de la derecha, de la siguiente manera:

	cat file.txt | grep "string"

---
### REFERENCIAS
https://www.codecademy.com/learn/learn-the-command-line/modules/learn-the-command-line-redirection/cheatsheet
