----
### OBJETIVO
The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

---
### DATOS DE ACCESO
	Servidor : ssh bandit6@bandit.labs.overthewire.org -p 2220
	Contraseña : P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

---
### SOLUCION
	bandit6@bandit:~$ ls
	bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
	/var/lib/dpkg/info/bandit7.password
	bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
	Contraseña : z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
---
### NOTAS ADICCIONALES
Para poder evitar los errores de falta de permisos se puede utilizar el código "2>/dev/null" que hacer que todos los errores se vallan al null o al vacío, pudiendo ver así los documentos que realmente tenemos permisos.
### User 
- File is owned by user _uname_ (numeric user ID allowed).
### Group
- File belongs to group _gname_ (numeric group ID allowed).

---
### REFERENCIAS
