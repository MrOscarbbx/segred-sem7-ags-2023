----
### OBJETIVO 

Theres tapping coming in from the wires. What's it saying `nc jupiter.challenges.picoctf.org 21610`.

---
### SOLUCION

Al entrar al netcat podemos ver esta salida:
``` bash
mrioso-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 21610
.--. .. -.-. --- -.-. - ..-. { -- ----- .-. ... ...-- -.-. ----- -.. ...-- .---- ... ..-. ..- -. ...-- ----. ----- ..--- ----- .---- ----. ..... .---- ----. } 
```
y claramente es codigo morse, asi que lo pasamos a un traductor y sacamos la llave:

![[Pasted image 20231024214513.png]]

---
### NOTAS ADICCIONALES
PICOCTF{M0RS3C0D31SFUN3902019519}

---
### REFERENCIAS
https://morsedecoder.com/es/