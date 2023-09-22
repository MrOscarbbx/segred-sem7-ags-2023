----
### OBJETIVO 
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.

---
### DATOS DE ACCESO
	Servidor : ssh bandit29@bandit.labs.overthewire.org -p 2220
	Contraseña : tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S

---
### SOLUCION
	Se crea una carpeta temporal como lo habiamos hecho anteriormente ...
	bandit29@bandit:/tmp/tmp.g8Ih88qYrc$ ls
	repo
	bandit29@bandit:/tmp/tmp.g8Ih88qYrc$ cd repo/
	bandit29@bandit:/tmp/tmp.g8Ih88qYrc/repo$ ls
	README.md
	bandit29@bandit:/tmp/tmp.g8Ih88qYrc/repo$ cat README.md
	# Bandit Notes
	Some notes for bandit30 of bandit.
	
	## credentials
	
	- username: bandit30
	- password: <no passwords in production!>
	bandit29@bandit:/tmp/tmp.g8Ih88qYrc/repo$ git branch -r
	  origin/HEAD -> origin/master
	  origin/dev
	  origin/master
	  origin/sploits-dev
	bandit29@bandit:/tmp/tmp.g8Ih88qYrc/repo$ git checkout dev
	Branch 'dev' set up to track remote branch 'dev' from 'origin'.
	Switched to a new branch 'dev'
	bandit29@bandit:/tmp/tmp.g8Ih88qYrc/repo$ cat README.md
	# Bandit Notes
	Some notes for bandit30 of bandit.
	
	## credentials
	
	- username: bandit30
	- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
---
### NOTAS ADICCIONALES

GIT Branch
	If --list is given, or if there are no non-option arguments, existing branches are listed; the current branch will be highlighted in green and marked with an asterisk. Any branches checked out in linked worktrees will be highlighted in cyan and marked with a plus sign. Option -r causes the remote-tracking branches to be listed, and option -a shows both local and remote branches.

---
### REFERENCIAS
https://git-scm.com/docs/git-branch#Documentation/git-branch.txt