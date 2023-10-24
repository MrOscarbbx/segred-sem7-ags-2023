----
### OBJETIVO 
Download this image and find the flag.

- [Download image](https://artifacts.picoctf.net/c/215/pico.flag.png)
---
### SOLUCION
Despues de buscar en los metadatos, en el hexadump, y buscar archivos dentro de la imagen y no encontrar nada,  solo quedaba buscar dentro de la imagen asi que usando esteganografía pude sacar la bandera

``` bash
┌──(kali㉿kali)-[~/Picoctf/segundoparcial/seg]
└─$ zsteg -a pico.flag.png | grep pico 
b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_96ae0ac1}$t3g0"
                 
```

---
### NOTAS ADICCIONALES

---
### REFERENCIAS
