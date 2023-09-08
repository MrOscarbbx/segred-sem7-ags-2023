----
### OBJETIVO 
The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on

---
### DATOS DE ACCESO
	Servidor : ssh bandit13@bandit.labs.overthewire.org -p 2220
	Contraseña : wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

---
### SOLUCION
	bandit13@bandit:~$ ls
		sshkey.private
	bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p 2220
		The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
		ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
		This key is not known by any other names
		Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
		Could not create directory '/home/bandit13/.ssh' (Permission denied).
		Failed to add the host to the list of known hosts (/home/bandit13/.ssh/known_hosts).
		                         _                     _ _ _
		                        | |__   __ _ _ __   __| (_) |_
		                        | '_ \ / _` | '_ \ / _` | | __|
		                        | |_) | (_| | | | | (_| | | |_
		                        |_.__/ \__,_|_| |_|\__,_|_|\__|
		
		
		                      This is an OverTheWire game server.
		            More information on http://www.overthewire.org/wargames
	bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
	Contraseña : fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

---
### NOTAS ADICCIONALES
**La clave SSH consiste en la generación de un par de claves** que proporcionan dos largas cadenas de caracteres —una pública y una privada—. La **clave pública** se instala en cualquier servidor y luego se desbloquea mediante la conexión con un cliente SSH que hace uso de la **clave privada**. Si las dos claves coinciden, el servidor SSH permite el acceso sin necesidad de utilizar una contraseña. No obstante, para añadir una capa de seguridad adicional, siempre podemos aumentar la protección de la clave privada usando una contraseña.

Usando el comando :

	ssh -i sshkey.private ...
Podemos entrar al servidor de la llave

---
### REFERENCIAS
