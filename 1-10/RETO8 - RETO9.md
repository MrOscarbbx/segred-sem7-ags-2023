----
### OBJETIVO 
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

---
### DATOS DE ACCESO
	Servidor : ssh bandit8@bandit.labs.overthewire.org -p 2220
	Contraseña : TESKZC0XvTetK0S9xNwm25STk5iWrBvP

---
### SOLUCION
	bandit8@bandit:~$ ls
		data.txt
	bandit8@bandit:~$ wc data.txt
		1001  1001 33033 data.txt
	bandit8@bandit:~$ cat data.txt | sort | uniq -u
	Contraseña : EN632PlfYiZbn3PhVK3XOGSlNInNE00t

---
### NOTAS ADICCIONALES
Para poder identificar las cadenas que son únicas existe el comando `uniq`, y para ordenar las cadenas de un documento se utiliza el comando `sort`
Cuando ordenamos el archivo, agrupa las líneas duplicadas y `uniq` las trata como duplicados. Usaremos `sort` en el archivo, canalizaremos la salida ordenada a `uniq`

---
### REFERENCIAS
https://nksistemas.com/comando-uniq-de-linux-explicado-con-ejemplos/

https://itsfoss.com/es/comando-sort-linux/

https://es.linux-console.net/?p=8248#gsc.tab=0