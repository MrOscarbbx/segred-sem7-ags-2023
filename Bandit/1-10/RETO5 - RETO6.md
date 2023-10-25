----
### OBJETIVO 
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable

---
### DATOS DE ACCESO
	Servidor : ssh bandit3@bandit.labs.overthewire.org -p 2220
	Contraseña : lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

---
### SOLUCION
	bandit5@bandit:~$ ls
		inhere
	bandit5@bandit:~$ cd inhere/
	bandit5@bandit:~/inhere$ ls
		maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15 maybehere18 maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16 maybehere19 maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
	bandit5@bandit:~/inhere$ find . -size 1033c
		./maybehere07/.file2
	bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
	Contraseña : P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

---
### NOTAS ADICCIONALES
En esta ocasión se va a necesitar que encontrar entre muchas carpetas un tipo especifico de documento, así que se necesita que utilizar el comando "find" que nos servirá para filtrar los documentos mediante diferentes tipos de características usando diferentes opciones o modificadores.
OPCIONES DE COMANDO FIND IMPORTANTES :
### TYPE
| Opcion | Accion |
|-|-|
|b |block (buffered) special|
|c |character (unbuffered) special|
|d |directory
|p |named pipe (FIFO)
|f |regular file
|l |symbolic link; this is never true if the **-L** option or the **-follow** option is in effect, unless the symbolic link is broken.  If you want to search for symbolic links when **-L** is in effect, use **-xtype**.
|s |socket
|D |door (Solaris)

### SIZE
| Opcion | Accion |
|-|-|
|b|    for 512-byte blocks (this is the default if no suffix is used)
|c|    for bytes
|w|    for two-byte words
|k|    for kibibytes (KiB, units of 1024 bytes)
|M|    for mebibytes (MiB, units of 1024 * 1024 = 1048576 bytes
|G|    for gibibytes (GiB, units of 1024 * 1024 * 1024 = 1073741824 bytes)


---
### REFERENCIAS
https://man7.org/linux/man-pages/man1/find.1.html
