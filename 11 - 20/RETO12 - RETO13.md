----
### OBJETIVO 
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

---
### DATOS DE ACCESO
	Servidor : ssh bandit12@bandit.labs.overthewire.org -p 2220
	Contraseña : JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

---
### SOLUCION
	bandit12@bandit:~$ xxd -r data.txt | file -
	/dev/stdin: gzip compressed data, was "data2.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix
	bandit12@bandit:~$ xxd -r data.txt | zcat | file -
		/dev/stdin: bzip2 compressed data, block size = 900k
	bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | file -
		/dev/stdin: gzip compressed data, was "data4.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix
	bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | file -
		/dev/stdin: POSIX tar archive (GNU)
	bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | file -
		/dev/stdin: POSIX tar archive (GNU)
	bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | file -
		/dev/stdin: bzip2 compressed data, block size = 900k
	bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | file -
		/dev/stdin: POSIX tar archive (GNU)
	bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | file -
		/dev/stdin: gzip compressed data, was "data9.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix
	bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file -
		/dev/stdin: ASCII text
	bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
		The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

---
### NOTAS ADICCIONALES

El Hexadecimal dump es una vista hexadecimal de los datos de la computadora, desde la memoria o desde un archivo de computadora o dispositivo de almacenamiento.
Para poder sacar el dump de un archivo utilizamos el comando

	xxd -r filename.txt

Existen diferentes tipo de archivos comprimidos, y para cada uno de ellos existen diferentes tipos de comandos para poder descomprimirlos, a continuación algunos de los comandos para poder descomprimir archivos:

| Comando | Tipo de archivo | Ver en Consola|
| - |- | - |
| unzip filename.zip | ZIP| 7z x
| unrar filname.rar | RAR | 7z x
|gzip -d filename.gz | GZIP| zcat
|bzip2 -d filename.bz| BZIP2| bzcat
| tar xvf filename.tar | TAR | tar xO


---
### REFERENCIAS

Diapositivas de la clase