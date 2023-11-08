----
### OBJETIVO 
What does asm1(0x6fa) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/b41e08fc19ceb9d0466ebd68d36c5630/test.S)

---
### SOLUCION

El lenguaje ensamblador podemos realizar operaciones de comparación y operaciones básicas como sumas restas y movimientos.
edp y esp son posiciones en la memoria, que usaremos como stack, a continuación explicare como se mueve el siguiente codigo
``` 
asm1:
        <+0>:   push   ebp <--Se le da el valor que entra a la funcion"0x6fa" a la primera posicion del stack
        <+1>:   mov    ebp,esp<--Se pone el inicio del stack ebp
        <+3>:   cmp    DWORD PTR [ebp+0x8],0x3a2<-- coparamos que es mas grande si el valor de la primera pocicion del stack o 0x3a2
```
``` python
>>> 0x6fa > 0x3a2
>>> True
```        
```
        <+10>:  jg     0x512 <asm1+37> si es verdad entonces se pide que se salte a la linea 37
        <+12>:  cmp    DWORD PTR [ebp+0x8],0x358
        <+19>:  jne    0x50a <asm1+29>
        <+21>:  mov    eax,DWORD PTR [ebp+0x8]
        <+24>:  add    eax,0x12
        <+27>:  jmp    0x529 <asm1+60>
        <+29>:  mov    eax,DWORD PTR [ebp+0x8]
        <+32>:  sub    eax,0x12
        <+35>:  jmp    0x529 <asm1+60>
        <+37>:  cmp    DWORD PTR [ebp+0x8],0x6fa<-- Ahora va a comparar la primer dato de el stack con 0x6fa
        <+44>:  jne    0x523 <asm1+54><--si no es igual entonces se pasa a la linea 54
```
```python
>>> 0x6fa > 0x6fa
>>> False
```
```
        <+46>:  mov    eax,DWORD PTR [ebp+0x8]<-- guarda en eax el elemento de la primera pocicion del stack
        <+49>:  sub    eax,0x12<-- se le resta a el valor de eax 0x12
```
``` python 
>>> 0x6fa - 0x12
>>> 1768
>>> hex(1768)
>>> '0x6e8'
```
```
        <+52>:  jmp    0x529 <asm1+60> <--Saltar hasta la linea 60
        <+54>:  mov    eax,DWORD PTR [ebp+0x8]
        <+57>:  add    eax,0x12
        <+60>:  pop    ebp <--sale el primer dato del stack
        <+61>:  ret <--se regresa el valor
```
---
### NOTAS ADICCIONALES

---
### REFERENCIAS
