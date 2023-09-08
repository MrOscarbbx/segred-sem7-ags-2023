----
### OBJETIVO 
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

---
### DATOS DE ACCESO
	Servidor : ssh bandit14@bandit.labs.overthewire.org -p 2220
	Contraseña :  fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

---
### SOLUCION
	bandit14@bandit:~$ nc localhost 30000
		fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
		Correct!
	Contraseña : jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
---
### NOTAS ADICCIONALES
The netcat command, also known as nc, is **a command-line utility that allows users to read and write data over a network connection**. It can be used to establish connections to servers and clients, send and receive data, and perform a variety of other network-related tasks.

---
### REFERENCIAS
https://www.tutorialspoint.com/the-netcat-command-in-linux#:~:text=The%20netcat%20command%2C%20also%20known,of%20other%20network%2Drelated%20tasks.