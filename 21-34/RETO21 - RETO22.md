----
### OBJETIVO 
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

---
### DATOS DE ACCESO
	Servidor : ssh bandit21@bandit.labs.overthewire.org -p 2220
	Contraseña : NvEJF7oVjkddltPSrdKEFOllh9V1IBcq

---
### SOLUCION

	bandit21@bandit:~$ ls -la /etc/cron.d
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
	bandit21@bandit:~$ cat /etc/cron.d/cronjob_bandit22
		@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
		* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
	bandit21@bandit:~$ cat /usr/bin/cronjob_bandit22.sh
		#!/bin/bash
		chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
		cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
	bandit21@bandit:~$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
		WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff

---
### NOTAS ADICCIONALES

**Cron** es un demonio (que es como se conoce a un proceso en segundo plano) que se ejecuta desde el mismo instante en el que arranca el sistema operativo. Cron se encargará de comprobar si existe alguna tarea (job) para ser ejecutada, de acuerdo a la hora configurada en el propio sistema operativo

**Crontab** es un archivo de texto, se trata de un archivo con un contenido especial y específicamente diseñado para que sea leído correctamente por Cron y proceder con la ejecución que nosotros hayamos programado.

---
### REFERENCIAS
https://www.redeszone.net/tutoriales/servidores/cron-crontab-linux-programar-tareas/