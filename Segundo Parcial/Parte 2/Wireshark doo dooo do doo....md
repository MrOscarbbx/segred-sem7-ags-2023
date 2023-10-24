----
### OBJETIVO 
Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/ea41c400c3c7b4a63406e5e607d362ab/shark1.pcapng).

---
### SOLUCION
Cuando revisamos la captura de paquetes podemos ver una cadena que parece una bandera pero encriptada
![[Pasted image 20231023225101.png]]
Usando rot13 decodificamos la contraseña:
``` bash
┌──(kali㉿kali)-[~]
└─$ echo "Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}" | rot13
The flag is picoCTF{p33kab00_1_s33_u_deadbeef}

```

---
### NOTAS ADICCIONALES

---
### REFERENCIAS
