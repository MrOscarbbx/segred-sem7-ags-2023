----
### OBJETIVO 
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

---
### SOLUCION
![[Pasted image 20231022225830.png]]

Si intentamos hacer lo mismo que en WebNet0 nos sale esto asi que tenemos que buscar de otra manera

![[Pasted image 20231022230350.png]]
Podemos ver que una imagen esta siendo manda en un paquete así que vamos a recuperarla para ver si ahi se encuentra la bandera
![[Pasted image 20231022231238.png]]
cuando extraemos la imagen y usamos un strings en ella podemos encontrar la bandera

picoCTF{honey.roasted.peanuts}


---
### NOTAS ADICCIONALES

---
### REFERENCIAS
