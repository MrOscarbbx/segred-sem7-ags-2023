----
### OBJETIVO 
There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo` via the port `2220`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

Clone the repository and find the password for the next level.

---
### DATOS DE ACCESO
	Servidor : ssh bandit27@bandit.labs.overthewire.org -p 2220
	Contraseña : YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS

---
### SOLUCION
	
	bandit27@bandit:~$ mktemp -d
		/tmp/tmp.H3YY5nQ8Zv
	bandit27@bandit:~$ cd /tmp/tmp.H3YY5nQ8Zv
	bandit27@bandit:/tmp/tmp.H3YY5nQ8Zv$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
		Cloning into 'repo'...
		The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
		ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
		This key is not known by any other names
		Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
		Could not create directory '/home/bandit27/.ssh' (Permission denied).
		Failed to add the host to the list of known hosts (/home/bandit27/.ssh/known_hosts).
	                         _                     _ _ _
	                        | |__   __ _ _ __   __| (_) |_
	                        | '_ \ / _` | '_ \ / _` | | __|
	                        | |_) | (_| | | | | (_| | | |_
	                        |_.__/ \__,_|_| |_|\__,_|_|\__|
	
	
	                      This is an OverTheWire game server.
	            More information on http://www.overthewire.org/wargames
	
	bandit27-git@localhost's password:
	remote: Enumerating objects: 3, done.
	remote: Counting objects: 100% (3/3), done.
	remote: Compressing objects: 100% (2/2), done.
	remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
	Receiving objects: 100% (3/3), done.
	bandit27@bandit:/tmp/tmp.H3YY5nQ8Zv$ ls -la
		total 10564
		drwx------    3 bandit27 bandit27     4096 Sep 21 03:46 .
		drwxrwx-wt 2765 root     root     10801152 Sep 21 03:47 ..
		drwxrwxr-x    3 bandit27 bandit27     4096 Sep 21 03:47 repo
		bandit27@bandit:/tmp/tmp.H3YY5nQ8Zv$ cd repo/
		bandit27@bandit:/tmp/tmp.H3YY5nQ8Zv/repo$ ls
		README
	bandit27@bandit:/tmp/tmp.H3YY5nQ8Zv/repo$ cat README
		The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR

---
### NOTAS ADICCIONALES
Puedes clonar un repositorio de GitHub.com en el equipo local o en un codespace, para que sea más fácil corregir conflictos de combinación, agregar o quitar archivos e insertar confirmaciones más grandes. Al clonar un repositorio, se copia el repositorio de GitHub.com en la máquina local o en una máquina virtual remota cuando se crea un codespace.

---
### REFERENCIAS
https://docs.github.com/es/repositories/creating-and-managing-repositories/cloning-a-repository