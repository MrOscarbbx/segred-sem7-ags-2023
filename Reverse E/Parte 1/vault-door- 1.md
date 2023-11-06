----
### OBJETIVO 
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/29b91e638ccbd76aaa8c0462d1c64d8d/VaultDoor1.java)

---
### SOLUCION
Solo tenemos que poner los datos en un un diccionario y imprimirlo de manera correcta
![[Pasted image 20231105205538.png]]

``` python
a = {0 : 'd',

29 : '3',

4 : 'r',

2 : '5',

23 : 'r',

3 : 'c',

17 : '4',

1 : '3',

7 : 'b',

10 : '_',

5 : '4',

9 : '3',

11 : 't',

15 : 'c',

8 : 'l',

12 : 'H',

20 : 'c',

14 : '_',

6 : 'm',

24 : '5',

18 : 'r',

13 : '3',

19 : '4',

21 : 'T',

16 : 'H',

27 : 'f',

30 : 'b',

25 : '_',

22 : '3',

28 : '6',

26 : 'f',

31 : '0'}

for i in range(0,len(a)):

    print(a[i],end="")
    
```
``` bash
PS C:\Users\mrosc\Documents\PSP> & C:/Users/mrosc/AppData/Local/Programs/Python/Python312/python.exe "c:/Users/mrosc/Documents/obsidian/segred-sem7-ags-2023/Reverse E/Parte 1/Revers1.py"
d35cr4mbl3_tH3_cH4r4cT3r5_ff63b0
```
---
### NOTAS ADICCIONALES

---
### REFERENCIAS
