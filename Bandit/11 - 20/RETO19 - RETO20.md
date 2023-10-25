----
### OBJETIVO 
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

---
### DATOS DE ACCESO
	Servidor : ssh bandit19@bandit.labs.overthewire.org -p 2220
	Contraseña : awhqfNnAbc1naukrpqDYcF95h7HoMTrC

---
### SOLUCION

	bandit19@bandit:~$ bandit19@bandit:~$ ls -la
		total 36
		drwxr-xr-x  2 root     root      4096 Apr 23 18:04 .
		drwxr-xr-x 70 root     root      4096 Apr 23 18:05 ..
		-rwsr-x---  1 bandit20 bandit19 14876 Apr 23 18:04 bandit20-do
		-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
		-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
		-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
	bandit19@bandit:~$ ./bandit20-do
		Run a command as another user.
		Example: ./bandit20-do id
	bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
	Contraseña : VxCazJaVykI6W36BkBU0mJTCM8rR95XT

---
### NOTAS ADICCIONALES

Hay archivos o directorios los cuales tienen permisos especiales "setuid" que nos permiten ejecutar acciones en nombre de otro usuario diferente a el de nosotros, estos permisos se ven reflejados en la columna de usuarios y grupo de los permisos de los archivos marcandolos con una "s"

---
### REFERENCIAS
