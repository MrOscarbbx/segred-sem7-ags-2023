----
### OBJETIVO 
What does asm2(0x4,0x21) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/7e3eb2f90200ac88126f62ceb4bc3948/test.S)

---
### SOLUCION
Vamos a ver que es lo que hace este codigo en ensamblador
```
[0x4] ret
[0x8] 0x4
[0xc] 0x21

[eax] 
asm2:
        <+0>:   push   ebp #Crea el stock
		<+1>:   mov    ebp,esp #inicio de el stock
        <+3>:   sub    esp,0x10 #Reserva espacios en la memora en para guardar datos
        <+6>:   mov    eax,DWORD PTR [ebp+0xc] # Crea la Inicialza eax con el valor de 0xc
        <+9>:   mov    DWORD PTR [ebp-0x4],eax # Se mueve a -0x4 lo que esta en -0x4
        <+12>:  mov    eax,DWORD PTR [ebp+0x8] # Se asigna a eax lo que esta en 0x8
        <+15>:  mov    DWORD PTR [ebp-0x8],eax # mover a -0x8 lo que esta en eax 
        <+18>:  jmp    0x509 <asm2+28> # salta a la linea 28
        <+20>:  add    DWORD PTR [ebp-0x4],0x1
        <+24>:  add    DWORD PTR [ebp-0x8],0x74
        <+28>:  cmp    DWORD PTR [ebp-0x8],0xfb46 # compara lo que esta en -0x8 con 0xfb46
        <+35>:  jle    0x501 <asm2+20> # compara si lo que esta en -0x8 es menor o igual a 0xfb46
        #Aqui se crea un loop en el cual se le esta sumando 1 a -0x4 y a -0x8 0x74, hasta que -0x8 llegue a 0xfb46  
        <+37>:  mov    eax,DWORD PTR [ebp-0x4] # Se esta asignando a eax el valor de -0x4
        #Para poder sacar el valor de -0x4 solo hay que ver cuantas vueltas dio el loop, asi que tenemos que dividir 0xfb46 entre 0x74 y sumarle eso a el valor de -0x4
```
``` python
>>> 0xfb46 / 0x74
554.5344827586207
>>> hex(0x21 + 555)
'0x24c'
```
```
        <+40>:  leave  
        <+41>:  ret    
```

---
### NOTAS ADICCIONALES

---
### REFERENCIAS
