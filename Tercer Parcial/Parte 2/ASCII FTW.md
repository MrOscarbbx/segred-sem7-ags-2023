----
### OBJETIVO 
This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program.You can download the file from [here](https://artifacts.picoctf.net/c/507/asciiftw).

---
### SOLUCION
Al correr el programa nos encontramos con lo siguiente:
```bash
mrioso@DESKTOP-A53VGNO:/mnt/c/Users/mrosc/terserparcial$ ./asciiftw
The flag starts with 70
```
En el codigo de el ejecutable podemos encontrar una lista de caracteres empezando en el 70 como dice el programa
```ASM

mrioso@DESKTOP-A53VGNO:/mnt/c/Users/mrosc/terserparcial$ objdump -d asciiftw
...
  1184:       c6 45 d0 70             movb   $0x70,-0x30(%rbp)
    1188:       c6 45 d1 69             movb   $0x69,-0x2f(%rbp)
    118c:       c6 45 d2 63             movb   $0x63,-0x2e(%rbp)
    1190:       c6 45 d3 6f             movb   $0x6f,-0x2d(%rbp)
    1194:       c6 45 d4 43             movb   $0x43,-0x2c(%rbp)
    1198:       c6 45 d5 54             movb   $0x54,-0x2b(%rbp)
    119c:       c6 45 d6 46             movb   $0x46,-0x2a(%rbp)
    11a0:       c6 45 d7 7b             movb   $0x7b,-0x29(%rbp)
    11a4:       c6 45 d8 41             movb   $0x41,-0x28(%rbp)
    11a8:       c6 45 d9 53             movb   $0x53,-0x27(%rbp)
    11ac:       c6 45 da 43             movb   $0x43,-0x26(%rbp)
    11b0:       c6 45 db 49             movb   $0x49,-0x25(%rbp)
    11b4:       c6 45 dc 49             movb   $0x49,-0x24(%rbp)
    11b8:       c6 45 dd 5f             movb   $0x5f,-0x23(%rbp)
    11bc:       c6 45 de 49             movb   $0x49,-0x22(%rbp)
    11c0:       c6 45 df 53             movb   $0x53,-0x21(%rbp)
    11c4:       c6 45 e0 5f             movb   $0x5f,-0x20(%rbp)
    11c8:       c6 45 e1 45             movb   $0x45,-0x1f(%rbp)
    11cc:       c6 45 e2 41             movb   $0x41,-0x1e(%rbp)
    11d0:       c6 45 e3 53             movb   $0x53,-0x1d(%rbp)
    11d4:       c6 45 e4 59             movb   $0x59,-0x1c(%rbp)
    11d8:       c6 45 e5 5f             movb   $0x5f,-0x1b(%rbp)
    11dc:       c6 45 e6 37             movb   $0x37,-0x1a(%rbp)
    11e0:       c6 45 e7 42             movb   $0x42,-0x19(%rbp)
    11e4:       c6 45 e8 43             movb   $0x43,-0x18(%rbp)
    11e8:       c6 45 e9 44             movb   $0x44,-0x17(%rbp)
    11ec:       c6 45 ea 39             movb   $0x39,-0x16(%rbp)
    11f0:       c6 45 eb 37             movb   $0x37,-0x15(%rbp)
    11f4:       c6 45 ec 31             movb   $0x31,-0x14(%rbp)
    11f8:       c6 45 ed 44             movb   $0x44,-0x13(%rbp)
    11fc:       c6 45 ee 7d             movb   $
```


``` JS
String.fromCharCode(0x70,0x69,0x63,0x6f,0x43,0x54,0x46,0x7b,0x41,0x53,0x43,0x49,0x49,0x5f,0x49,0x53,0x5f,0x45,0x41,0x53,0x59,0x5f,0x37,0x42,0x43,0x44,0x39,0x37,0x31,0x44,0x7d)
'picoCTF{ASCII_IS_EASY_7BCD971D}'
```
---
### NOTAS ADICCIONALES

---
### REFERENCIAS
