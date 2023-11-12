----
### OBJETIVO 
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/cd51b2c95be9f3626db6fe6665afb5a3/need-for-speed).

---
### SOLUCION
Para este ejecutable al momento de correrlo va muy rapido lo que pasa asi que usando un debugger y creando breaks en el programa main, analizando el main podemos ver que tiene metodos para poder recuperar las llaves unicas de cada usuario, y para imprimir las banderas 
``` bash
mrioso-picoctf@webshell:~/reversing$ ls
SafeOpener.class  gdbme  need-for-speed  rev  rev_this  test.S  test.S.1  test.S.2
mrioso-picoctf@webshell:~/reversing$ ./need-for-speed 
Keep this thing over 50 mph!
============================

Creating key...
Not fast enough. BOOM!

mrioso-picoctf@webshell:~/reversing$ gdb need-for-speed 
GNU gdb (Ubuntu 12.0.90-0ubuntu1) 12.0.90
Copyright (C) 2022 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from need-for-speed...
(No debugging symbols found in need-for-speed)
(gdb) set disassembly-flavor intel
(gdb) disassemble main
Dump of assembler code for function main:
   0x000000000000091a <+0>:     push   rbp
   0x000000000000091b <+1>:     mov    rbp,rsp
   0x000000000000091e <+4>:     sub    rsp,0x10
   0x0000000000000922 <+8>:     mov    DWORD PTR [rbp-0x4],edi
   0x0000000000000925 <+11>:    mov    QWORD PTR [rbp-0x10],rsi
   0x0000000000000929 <+15>:    mov    eax,0x0
   0x000000000000092e <+20>:    call   0x8d8 <header>
   0x0000000000000933 <+25>:    mov    eax,0x0
   0x0000000000000938 <+30>:    call   0x82f <set_timer>
   0x000000000000093d <+35>:    mov    eax,0x0
   0x0000000000000942 <+40>:    call   0x87d <get_key>
   0x0000000000000947 <+45>:    mov    eax,0x0
   0x000000000000094c <+50>:    call   0x8ac <print_flag>
   0x0000000000000951 <+55>:    mov    eax,0x0
   0x0000000000000956 <+60>:    leave  
   0x0000000000000957 <+61>:    ret    
End of assembler dump.
(gdb) break main
Breakpoint 1 at 0x91e
(gdb) run
Starting program: /home/mrioso-picoctf/reversing/need-for-speed 
warning: Error disabling address space randomization: Operation not permitted
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".

Breakpoint 1, 0x000055cb9880091e in main ()
(gdb) disassemble main
Dump of assembler code for function main:
   0x000055cb9880091a <+0>:     push   rbp
   0x000055cb9880091b <+1>:     mov    rbp,rsp
=> 0x000055cb9880091e <+4>:     sub    rsp,0x10
   0x000055cb98800922 <+8>:     mov    DWORD PTR [rbp-0x4],edi
   0x000055cb98800925 <+11>:    mov    QWORD PTR [rbp-0x10],rsi
   0x000055cb98800929 <+15>:    mov    eax,0x0
   0x000055cb9880092e <+20>:    call   0x55cb988008d8 <header>
   0x000055cb98800933 <+25>:    mov    eax,0x0
   0x000055cb98800938 <+30>:    call   0x55cb9880082f <set_timer>
   0x000055cb9880093d <+35>:    mov    eax,0x0
   0x000055cb98800942 <+40>:    call   0x55cb9880087d <get_key>
   0x000055cb98800947 <+45>:    mov    eax,0x0
   0x000055cb9880094c <+50>:    call   0x55cb988008ac <print_flag>
   0x000055cb98800951 <+55>:    mov    eax,0x0
   0x000055cb98800956 <+60>:    leave  
   0x000055cb98800957 <+61>:    ret    
End of assembler dump.
(gdb) call (int) get_key()
Creating key...
Finished
$1 = 9
(gdb) call (int) print_flag()
Printing flag:
PICOCTF{Good job keeping bus #24c43740 speeding along!}
$2 = 56
```
---
### NOTAS ADICCIONALES

---
### REFERENCIAS
