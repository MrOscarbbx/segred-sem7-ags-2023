----
### OBJETIVO 
Download this image file and find the flag.

- [Download image file](https://artifacts.picoctf.net/c/102/drawing.flag.svg)
---
### SOLUCION
si descargamos el documento y lo abrimos en el navegador y revisamos el codigo fuente de la imagen podemos ver como se va formando la bandera en las diferentes vectores de la imagen, solo es cuestion de juntarlos: 
![[Pasted image 20231023230212.png]]

``` bash
┌──(kali㉿kali)-[~/Picoctf/segundoparcial/enhance]
└─$ echo "{ 3 n h 4 n c 3 d _ d 0 a 7 5 7 b f }" | tr -d " "
{3nh4nc3d_d0a757bf}
```
picoCTF{3nh4nc3d_d0a757bf}

---
### NOTAS ADICCIONALES

---
### REFERENCIAS
