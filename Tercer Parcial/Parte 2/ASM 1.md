----
### OBJETIVO 
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt).

---
### SOLUCION
```BASH
mrioso@DESKTOP-A53VGNO:/mnt/c/Users/mrosc/terserparcial$ cat disassembler-dump0_a.txt
<+0>:     endbr64
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x4],edi
<+11>:    mov    QWORD PTR [rbp-0x10],rsi
<+15>:    mov    eax,0x30
<+20>:    pop    rbp
<+21>:    ret
```
Podemos ver que a eax se le asigna el valor de 0x30 en la linea 15 asi que solo es cuestion de transformarlo a ascii
nos da 48
picoCTF{48}

---
### NOTAS ADICCIONALES

---
### REFERENCIAS
