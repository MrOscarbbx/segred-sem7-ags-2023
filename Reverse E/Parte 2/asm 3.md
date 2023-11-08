----
### OBJETIVO 
What does asm3(0xd2c26416,0xe6cf51f0,0xe54409d5) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/df999527eaecf46f259c4337a820856c/test.S)

---
### SOLUCION

```
asm3:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   xor    eax,eax
        <+5>:   mov    ah,BYTE PTR [ebp+0x9]
        <+8>:   shl    ax,0x10
        <+12>:  sub    al,BYTE PTR [ebp+0xe]
        <+15>:  add    ah,BYTE PTR [ebp+0xf]
        <+18>:  xor    ax,WORD PTR [ebp+0x12]
        <+22>:  nop
        <+23>:  pop    ebp
        <+24>:  ret  
```
Podemos utilizar un emulador para poder realizar las operaciones de manera mas sencilla, tan solo tenemos que meter los datos que se pasa a el stack y mandar llamar el metodo:
al final el valor de eax es el que nos da la bandera
![[Pasted image 20231107220842.png]]
bandera 0x00000375

---
### NOTAS ADICCIONALES

---
### REFERENCIAS
Emulador: https://carlosrafaelgn.com.br/Asm86/