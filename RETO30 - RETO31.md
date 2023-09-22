----
### OBJETIVO 
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo` via the port `2220`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.

---
### DATOS DE ACCESO
	Servidor : ssh bandit30@bandit.labs.overthewire.org -p 2220
	Contraseña : xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS

---
### SOLUCION
	SE CREA EL DIRECTORIO Y EL REPOSITORIO COMO ANTES...
	
	bandit30@bandit:/tmp/tmp.DbvopKxvhi/repo$ ls
	README.md
	bandit30@bandit:/tmp/tmp.DbvopKxvhi/repo$ cat README.md
	just an epmty file... muahaha
	bandit30@bandit:/tmp/tmp.DbvopKxvhi/repo$ git log
	commit 59530d30d299ff2e3e9719c096ebf46a65cc1424 (HEAD -> master, origin/master, origin/HEAD)
	Author: Ben Dover <noone@overthewire.org>
	Date:   Sun Apr 23 18:04:42 2023 +0000
	
	    initial commit of README.md
	bandit30@bandit:/tmp/tmp.DbvopKxvhi/repo$ git branch -r
	  origin/HEAD -> origin/master
	  origin/master
	bandit30@bandit:/tmp/tmp.DbvopKxvhi/repo$ git tag
	secret
	bandit30@bandit:/tmp/tmp.DbvopKxvhi/repo$ git show secret
	OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt

---
### NOTAS ADICCIONALES
Git tag:
	Como muchos VCS, Git tiene la posibilidad de etiquetar puntos específicos del historial como importantes. Esta funcionalidad se usa típicamente para marcar versiones de lanzamiento (v1.0, por ejemplo). En esta sección, aprenderás cómo listar las etiquetas disponibles, cómo crear nuevas etiquetas y cuáles son los distintos tipos de etiquetas.
	Git utiliza dos tipos principales de etiquetas: ligeras y anotadas.
	Una etiqueta ligera es muy parecido a una rama que no cambia - simplemente es un puntero a un _commit_ específico.
	Sin embargo, las etiquetas anotadas se guardan en la base de datos de Git como objetos enteros. Tienen un _checksum_; contienen el nombre del etiquetador, correo electrónico y fecha; tienen un mensaje asociado; y pueden ser firmadas y verificadas con _GNU Privacy Guard_ (GPG). Normalmente se recomienda que crees etiquetas anotadas, de manera que tengas toda esta información; pero si quieres una etiqueta temporal o por alguna razón no estás interesado en esa información, entonces puedes usar las etiquetas ligeras.
	
---
### REFERENCIAS
https://git-scm.com/book/es/v2/Fundamentos-de-Git-Etiquetado