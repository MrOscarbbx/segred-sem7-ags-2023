----
### OBJETIVO 
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

---
### SOLUCION
![[Pasted image 20231022224620.png]]
Al abrir el archivo de captura podemos ver un stream TLS, el cual si seguimos
![[Pasted image 20231022224725.png]]
No nos muestra nada, asi que tenemos que introducir la llave para que nos de acceso a el stream tls
![[Pasted image 20231022225014.png]]
Ahora si una ves que tenemos acceso a los paquetes tls, hacemos una busqueda para poder encontrar la bandera:
![[Pasted image 20231022225202.png]]

Pico-Flag: picoCTF{nongshim.shrimp.crackers}

---
### NOTAS ADICCIONALES
Seguridad de la capa de transporte (en inglés: Transport Layer Security, TLS) y su antecesor Secure Sockets Layer (SSL; en español capa de puertos seguros) son protocolos criptográficos, que proporcionan comunicaciones seguras por una red, comúnmente Internet.1​El protocolo TLS es el sucesor de SSL (1995), se introdujo en 1999 con una versión mejorada de SSL 3.0 al principio se llamó SSL 3.1. La versión actual es TLS 1.3 (a partir de 2018) Las versiones de SSL están desactualizadas y se consideran inseguras

---
### REFERENCIAS
https://es.wikipedia.org/wiki/Seguridad_de_la_capa_de_transporte