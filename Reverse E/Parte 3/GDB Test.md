----
### OBJETIVO 
Can you get the flag?Download this [binary](https://artifacts.picoctf.net/c/87/gdbme).Here's the test drive instructions:

- `$ chmod +x gdbme`
- `$ gdb gdbme`
- `(gdb) layout asm`
- `(gdb) break *(main+99)`
- `(gdb) run`
- `(gdb) jump *(main+104)`
---
### SOLUCION
Basicamente seguí las indicaciones del reto:

![[Pasted image 20231112124620.png]]
![[Pasted image 20231112124903.png]]
picoCTF{d3bugg3r_dr1v3_7776d758}

---
### NOTAS ADICCIONALES
GDB o GNU Debugger es el depurador estándar para el compilador GNU. Es un depurador portable que se puede utilizar en varias plataformas Unix y funciona para varios lenguajes de programación como C, C++ y Fortran. GDB fue escrito por Richard Stallman en 1986. GDB es software libre distribuido bajo la licencia GPL.

---
### REFERENCIAS
https://es.wikipedia.org/wiki/GNU_Debugger
