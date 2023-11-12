----
### OBJETIVO 
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev_this). Can you reverse the flag.

---
### SOLUCION
usando la herramienta que nos recomiendan las pistas ghidra, podemos ver que solo se esta leyendo los datos dentro de las llaves de picoCTF, y que a cada caracter inpar se le suma 5 y a cada caracter par se le restan 2
![[Pasted image 20231112171141.png]]
entonces podemos crear un script en python que pueda converir la bandera de regreso sumando 2 y restando 5
``` python
flag = ""
archivo =  open("rev_this","r").read() 
for i in range(8,len(archivo) -1):  
        if i & 1 == 0:
                flag += chr( ord(archivo[i]) - 5 )
        else:   
                flag += chr( ord(archivo[i]) + 2 )

print(f"picoCTF{{{flag}}}")
```

``` bash
┌──(kali㉿kali)-[~]
└─$ python exp.py
picoCTF{r3v3rs37ee84d27}
```


---
### NOTAS ADICCIONALES

---
### REFERENCIAS
