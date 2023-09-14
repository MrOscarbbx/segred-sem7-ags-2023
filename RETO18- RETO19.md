----
### OBJETIVO 
The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.

---
### DATOS DE ACCESO
	Servidor : ssh bandit18@bandit.labs.overthewire.org -p 2220
	Contraseña : hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg

---
### SOLUCION
	C:\Users\miste>ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
	                         _                     _ _ _
	                        | |__   __ _ _ __   __| (_) |_
	                        | '_ \ / _` | '_ \ / _` | | __|
	                        | |_) | (_| | | | | (_| | | |_
	                        |_.__/ \__,_|_| |_|\__,_|_|\__|
	
	
	                      This is an OverTheWire game server.
	            More information on http://www.overthewire.org/wargames
	bandit18@bandit.labs.overthewire.org's password:
	Contraseña : awhqfNnAbc1naukrpqDYcF95h7HoMTrC

---
### NOTAS ADICCIONALES
Básicamente lo que se realizo en este ejercicio es que directamente al momento de que estamos entrando a el servidor, realizamos un comando ya que el archivo bash esta modificado para que se ejecute un exit al momento de entrar al servidor

también podríamos ejecutar :

	bin/bash

que correría una consola dentro de la misma consola para que no se ejecute el exit

---
### REFERENCIAS
