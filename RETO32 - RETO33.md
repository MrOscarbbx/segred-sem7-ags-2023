----
### OBJETIVO 
After all this `git` stuff its time for another escape. Good luck!

---
### DATOS DE ACCESO
	Servidor : ssh bandit32@bandit.labs.overthewire.org -p 2220
	Contraseña : rmCBvG56y58BXzv98yZGdO7ATVL5dW8y

---
### SOLUCION
	WELCOME TO THE UPPERCASE SHELL
	ls
	sh: 1: LS: Permission denied
	$0
	$vim
	
![[Pasted image 20230922110241.png]]
	
	Contraseña : odHo63fHiFqcWWJG9rLiLDtPm45KzUKy

---
### NOTAS ADICCIONALES
As you know, the `$` sign in the bash is used to indicate the variables. This is a variable too but a different one.

The `$0` is one of [the special variables you get in bash](https://linuxhandbook.com/bash-special-variables/) and is used to print the filename of the script that is currently being executed.

The `$0` variable can be used in two ways in Linux:

- Use `$0` to find the [logged-in shell](https://linuxhandbook.com/login-shell/)
- Use `$0` to print the name of the script that is being executed

![[Pasted image 20230922110717.png]]

---
### REFERENCIAS
https://linuxhandbook.com/bash-dollar-0/