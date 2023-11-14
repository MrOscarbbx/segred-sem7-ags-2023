----
### OBJETIVO 
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.Download the corrupted message [here](https://artifacts.picoctf.net/c/193/message.txt)

---
### SOLUCION

```bash
mrioso-picoctf@webshell:~/tercer_parcial$ cat message.txt
heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V9AAB1F8}7
mrioso-picoctf@webshell:~/tercer_parcial$ python exp.py 
The flag is picoCTF{7R4N5P051N6_15_3XP3N51V3_A9AFB178}
```
para poder sacar la contraseña hice este script que toma los bloques de 3 caracteres y los mueve una posicion
```python

bandera = open("message.txt","r").read()

cont=0
bloque=""
banderaRes=""
for i in range(len(bandera)):
        if cont==3:
                banderaRes+=bloque[2]
                banderaRes+=bloque[0]
                banderaRes+=bloque[1]
                bloque=""
                bloque+=bandera[i]
                cont=1
        else:
                bloque+=bandera[i]
                cont+=1
banderaRes+=bloque[2]
banderaRes+=bloque[0]
banderaRes+=bloque[1]
print(banderaRes)
```
---
### NOTAS ADICCIONALES

---
### REFERENCIAS
