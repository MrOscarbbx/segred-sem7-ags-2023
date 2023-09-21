----
### OBJETIVO 
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

---
### DATOS DE ACCESO
	Servidor : ssh bandit22@bandit.labs.overthewire.org -p 2220
	Contraseña : WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff

---
### SOLUCION
	bandit22@bandit:~$ ls -la /etc/cron.d/
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

	bandit22@bandit:~$ cat /etc/cron.d/cronjob_bandit23
	@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
	* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
	bandit22@bandit:~$ cat /usr/bin/cronjob_bandit23.sh
	#!/bin/bash
	
	myname=$(whoami)
	mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)
	
	echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"
	
	cat /etc/bandit_pass/$myname > /tmp/$mytarget
	bandit22@bandit:~$ myname=bandit23
	bandit22@bandit:~$ mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)
	bandit22@bandit:~$ echo $mytarget
	8ca319486bfbbc3663ea0fbe81326349
	bandit22@bandit:~$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
	Contraseña : QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G

---
### NOTAS ADICCIONALES

El comando md5sum imprime una suma de verificación de 32 caracteres (128 bits) del archivo dado, utilizando el algoritmo MD5. La siguiente es la sintaxis de comandos de esta herramienta de línea de comandos:

	md5sum [OPTION]... [FILE]...

---
### REFERENCIAS
https://es.linux-console.net/?p=3436#gsc.tab=0
