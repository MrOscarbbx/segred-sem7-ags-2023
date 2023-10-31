----
### OBJETIVO 
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/237/atbash.jpg).

---
### SOLUCION

![[atbash.jpg]]
Solo nos sale una imagen, buscando en los meta datos y en buscando archivos dentro del archivo no encontre nada asi que lo que estamos buscando debe de estar escondido, asi que buscando con steghide podemos sacar la informacion oculta
``` bash
mrioso-picoctf@webshell:~/crypto$ steghide extract -sf atbash.jpg 
Enter passphrase: 
wrote extracted data to "encrypted.txt".
mrioso-picoctf@webshell:~/crypto$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_05y2z65z}

```
Teniendo esta cadena encriptada y asumiendo que se esta utilizando atrash cipher para poder encriptar la bandera solo vamos a un desencriptador de atrash y listo:
![[Pasted image 20231030225732.png]]
picoCTF{atbash_crack_05b2a65a}

---
### NOTAS ADICCIONALES
Steghide **es un programa de esteganografía que permite ocultar datos en varios tipos de imagen y archivos de audio**. Sus características incluyen el compactado y encriptado de los datos adjuntos, y la revisión automática de integridad usando un checksum

---
### REFERENCIAS
https://byte-mind.net/oculta-tus-datos-una-imagen-steghide-kali-linux/#:~:text=Steghide%20es%20un%20programa%20de,de%20integridad%20usando%20un%20checksum.