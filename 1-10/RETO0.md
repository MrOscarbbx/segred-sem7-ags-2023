- # Reto 0
### Objetivo 
Empezamos leyendo los requerimientos para poder completar el reto que son: 
		`The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is **bandit0** and the password is bandit0. Once logged in, go to the [Level 1](https://overthewire.org/wargames/bandit/bandit1.html) page to find out how to beat Level 1.

---
### Datos de Acceso
	Server : bandit.labs.overthewire.org
	User : bandit0
	Password : bandit0
---
### Comandos 
| **Comando** | **Descripcion** |
|-|-|
| pdw | Indica el directorio actual |
| whoami | Indica el usuario en el cual nos estamos logeados|
|cd /| Me lleva al directorio raiz|
| ls| Muestra los diferentes archivos del directorio actual|

---
Teniendo en cuenta esta informacion, buscamos cual es la sintaxis para poder conectarnos a el servidor, que es la siguiente:
		- `$ ssh <username>@<remote>`
		- `If you want to specify a port, add -p 0000, (replace 0000 with the desired port number).´
	Cambiamos los espacios con los datos que ya tenemos :
	- `ssh bandit0@bandit.labs.overthewire.org -p 2220
	Y con eso se completa el Reto 0