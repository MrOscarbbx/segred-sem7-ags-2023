----
### OBJETIVO 
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

---
### DATOS DE ACCESO
	Servidor : ssh bandit15@bandit.labs.overthewire.org -p 2220
	Contraseña : jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

---
### SOLUCION
	bandit15@bandit:~$ openssl s_client -connect localhost:30001
		CONNECTED(00000003)
		Can't use SSL_get_servername
		depth=0 CN = localhost
		verify error:num=18:self-signed certificate
		verify return:1
		depth=0 CN = localhost
		verify error:num=10:certificate has expired
		notAfter=Sep  7 12:45:10 2023 GMT
		verify return:1
		depth=0 CN = localhost
		notAfter=Sep  7 12:45:10 2023 GMT
		verify return:1
		    Start Time: 1694137139
		    Timeout   : 7200 (sec)
		    Verify return code: 10 (certificate has expired)
		    Extended master secret: no
		    Max Early Data: 0
		read R BLOCK
		jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
	Correct!
	Contraseña : JQttfApK4SeyHwDlI9SXGR50qclOAil1

---
### NOTAS ADICCIONALES
OpenSSL is a cryptography software library or toolkit that makes communication over computer networks more secure. The OpenSSL program is a command-line tool for using the various cryptography functions of OpenSSL’s crypto library from the shell. It is generally used for Transport Layer Security(TSL) or Secure Socket Layer(SSL) protocols. OpenSSL is licensed under an apache-style license, which means that under some simple license conditions, one can use the toolkit for commercial or non-commercial purposes.

---
### REFERENCIAS
https://www.geeksforgeeks.org/practical-uses-of-openssl-command-in-linux/