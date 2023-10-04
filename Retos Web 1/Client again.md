## Solucion

Primero revisamos la pagina
![[Pasted image 20231002113112.png]]
Revisamos el Cliente como en el ejercicio anterior
![[Pasted image 20231002113056.png]]
Vemos que la validacion esta en un codigo de javascript que esta obsecado asi que usando un desobsecador podemos ver el siguiente codigo
![[Pasted image 20231002113635.png]]
Podemos ver una funcion llamada  _ 0x4b5b() que esta trayendo los datos para ser verificados, asi que usando la consola de javascript que tiene el inspector de paginas le hacemos llamada a todos los datos para ver que se esta verificando
![[Pasted image 20231003233629.png]]

Y nos da como resultado lo siguiente:

	_0x4b5b('0x3')
	'picoCTF{'
	_0x4b5b('0x4')
	'not_this'
	_0x4b5b('0x5')
	'37115}'
	_0x4b5b('0x6')
	'_again_3'
	_0x4b5b('0x7')
	'this'
	_0x4b5b('0x8')
	'Password Verified'
	_0x4b5b('0x9')
	'Incorrect password'

Usando un poco de nuestra intuision podemos formar la bandera:
	picoCTF{not_this_again_337115}