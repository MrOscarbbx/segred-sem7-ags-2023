----
### OBJETIVO 
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).

---
### SOLUCION
```asm

mrioso@DESKTOP-A53VGNO:/mnt/c/Users/mrosc/terserparcial$ cat disassembler-dump0_b.txt
<+0>:     endbr64
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a
<+22>:    mov    eax,DWORD PTR [rbp-0x4]
<+25>:    pop    rbp
<+26>:    ret

```
podemos ver que en la linea 15 se le esta asignando a la pocicion 0x4 el valor 0x9fe1a y despues en la linea 22 se le da ese valo a eax , y podemos ver que es una base 16 asi que solo es cuenstion de pasarlo a ascii

picoCTF{654874}

---
### NOTAS ADICCIONALES

---
### REFERENCIAS
https://gchq.github.io/CyberChef/#recipe=From_Base(16)&input=MHg5ZmUxYQ