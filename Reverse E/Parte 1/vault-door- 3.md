----
### OBJETIVO 
This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://jupiter.challenges.picoctf.org/static/a648ca6dd275b9454c5d0de6d0f6efd3/VaultDoor3.java)

---
### SOLUCION
Si procesamos la cadena que tenemos para poder verificar la contraseña, con el mismo for que tenemos para procesar el input, podemos sacar la bandera
para esto podemos usar una consola de javascript

``` js
var password = "jU5t_a_sna_3lpm18gb41_u_4_mfr340"
var buffer = Array(32)
for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        }
buffer.join("")
'jU5t_a_s1mpl3_an4gr4m_4_u_1fb380'
```
---
### NOTAS ADICCIONALES

---
### REFERENCIAS
