----
### OBJETIVO 
There is a git repository at `ssh://bandit31-git@localhost/home/bandit31-git/repo` via the port `2220`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

Clone the repository and find the password for the next level.

---
### DATOS DE ACCESO
	Servidor : ssh bandit31@bandit.labs.overthewire.org -p 2220
	Contraseña : OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt

---
### SOLUCION
	bandit31@bandit:/tmp/tmp.rlUYspLkqV$ ls
	repo
	bandit31@bandit:/tmp/tmp.rlUYspLkqV$ cd repo/
	bandit31@bandit:/tmp/tmp.rlUYspLkqV/repo$ ls
	README.md
	bandit31@bandit:/tmp/tmp.rlUYspLkqV/repo$ cat README.md
	This time your task is to push a file to the remote repository.
	
	Details:
	    File name: key.txt
	    Content: 'May I come in?'
	    Branch: master
	
	bandit31@bandit:/tmp/tmp.rlUYspLkqV/repo$ echo "May I come in?" > key.txt
	bandit31@bandit:/tmp/tmp.rlUYspLkqV/repo$ ls
	key.txt  README.md
	bandit31@bandit:/tmp/tmp.rlUYspLkqV/repo$ git add -f key.txt
	bandit31@bandit:/tmp/tmp.rlUYspLkqV/repo$ git commit -m key.txt
	[master 54a0e02] key.txt
	 1 file changed, 1 insertion(+)
	 create mode 100644 key.txt
	bandit31@bandit:/tmp/tmp.rlUYspLkqV/repo$ git push origin master
	The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
	ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
	This key is not known by any other names
	Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
	Could not create directory '/home/bandit31/.ssh' (Permission denied).
	Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
	                         _                     _ _ _
	                        | |__   __ _ _ __   __| (_) |_
	                        | '_ \ / _` | '_ \ / _` | | __|
	                        | |_) | (_| | | | | (_| | | |_
	                        |_.__/ \__,_|_| |_|\__,_|_|\__|
	
	
	                      This is an OverTheWire game server.
	            More information on http://www.overthewire.org/wargames
	
	bandit31-git@localhost's password:
	Enumerating objects: 4, done.
	Counting objects: 100% (4/4), done.
	Delta compression using up to 2 threads
	Compressing objects: 100% (2/2), done.
	Writing objects: 100% (3/3), 322 bytes | 322.00 KiB/s, done.
	Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
	remote: ### Attempting to validate files... ####
	remote:
	remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
	remote:
	remote: Well done! Here is the password for the next level:
	remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
	remote:
	remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
	remote:
	To ssh://localhost:2220/home/bandit31-git/repo
	 ! [remote rejected] master -> master (pre-receive hook declined)
	error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'

---
### NOTAS ADICCIONALES

Git Add:
	The `git add` command adds a change in the working directory to the staging area. It tells Git that you want to include updates to a particular file in the next commit. However, `git add` doesn't really affect the repository in any significant way—changes are not actually recorded until you run `git commit`.

	_git add_ [--verbose | -v] [--dry-run | -n] [--force | -f] [--interactive | -i] [--patch | -p]
	  [--edit | -e] [--[no-]all | --[no-]ignore-removal | [--update | -u]] [--sparse]
	  [--intent-to-add | -N] [--refresh] [--ignore-errors] [--ignore-missing] [--renormalize]
	  [--chmod=(+|-)x] [--pathspec-from-file=<file> [--pathspec-file-nul]]
	  [--] [<pathspec>…​]
	
Git commit:
	Create a new commit containing the current contents of the index and the given log message describing the changes. The new commit is a direct child of HEAD, usually the tip of the current branch, and the branch is updated to point to it (unless no branch is associated with the working tree, in which case HEAD is "detached" as described in [git-checkout[1]](https://git-scm.com/docs/git-checkout)).

	_git commit_ [-a | --interactive | --patch] [-s] [-v] [-u<mode>] [--amend]
	   [--dry-run] [(-c | -C | --squash) <commit> | --fixup [(amend|reword):]<commit>)]
	   [-F <file> | -m <msg>] [--reset-author] [--allow-empty]
	   [--allow-empty-message] [--no-verify] [-e] [--author=<author>]
	   [--date=<date>] [--cleanup=<mode>] [--[no-]status]
	   [-i | -o] [--pathspec-from-file=<file> [--pathspec-file-nul]]
	   [(--trailer <token>[(=|:)<value>])…​] [-S[<keyid>]]
	   [--] [<pathspec>…​]

Git push:
	El comando git push en Git **se utiliza para cargar cambios locales en un repositorio remoto**. De esta manera, los commit locales se ponen a disposición de otros colaboradores del proyecto, quienes pueden recuperarlos a través de una búsqueda e incorporarlos a sus respectivos repositorios locales.

---
### REFERENCIAS
https://git-scm.com/docs/git-add
https://git-scm.com/docs/git-commit
https://aulab.es/articulos-guias-avanzadas/91/el-comando-git-push-en-git#:~:text=El%20comando%20git%20push%20en%20Git%20se%20utiliza%20para%20cargar,a%20sus%20respectivos%20repositorios%20locales.