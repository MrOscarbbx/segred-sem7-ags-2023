----
### OBJETIVO 

There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think

---
### DATOS DE ACCESO
	Servidor : ssh bandit20@bandit.labs.overthewire.org -p 2220
	Contraseña : VxCazJaVykI6W36BkBU0mJTCM8rR95XT

---
### SOLUCION

	bandit20@bandit:~$ ls
	suconnect
	bandit20@bandit:~$ ls -la
		total 36
		drwxr-xr-x  2 root     root      4096 Apr 23 18:04 .
		drwxr-xr-x 70 root     root      4096 Apr 23 18:05 ..
		-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
		-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
		-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
		-rwsr-x---  1 bandit21 bandit20 15600 Apr 23 18:04 suconnect
		bandit20@bandit:~$ ./suconnect
		Usage: ./suconnect <portnumber>
		This program will connect to the given port on localhost using TCP. If it receives the correct password from the other side, the next password is transmitted back.
		bandit20@bandit:~$ nc -lnvp 5050 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
		[1] 3319998
	bandit20@bandit:~$ Listening on 0.0.0.0 5050
	
	bandit20@bandit:~$ ./suconnect 5050
		Connection received on 127.0.0.1 36590
		Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
		Password matches, sending next password
		Contraseña : NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
	
---
### NOTAS ADICCIONALES
Anterior mente en el ejercicio 14 ya habíamos utilizado nc que es un comando que nos permite leer o escribir información en una conexión, solo que esta ves utilizamos algunas de sus fuciones:

- -a muestra información sobre todas las conexiones/sockets (tanto TCP y UDP)
- -p muestra los procesos que están usando las conexiones (sólo si lo ejecuta el superusuario)
- -l muestra información sobre las conexiones/sockets en modo escucha
- -e información en formato extendido
- -t sólo conexiones TCP, -u sólo conexiones UDP
- -v es usada para mostrar verbose output
- -n Suppress name/port resolutions

Lo que hacemos es con nc, abrimos el puerto 5050 y ponemos la contraseña de el nivel para que cuando se conecte el suconect reciba la contraseña y nos regrese la contraseña del nuevo nivel.

---
### REFERENCIAS
https://phoenixnap.com/kb/nc-command