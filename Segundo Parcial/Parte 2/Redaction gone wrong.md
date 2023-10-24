----
### OBJETIVO 
Now you DON’T see me.This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?

---
### SOLUCION
``` bash
┌──(kali㉿kali)-[~/Picoctf/segundoparcial/redactiongone]
└─$ pdftotext Financial_Report_for_ABC_Labs.pdf
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/segundoparcial/redactiongone]
└─$ ls
Financial_Report_for_ABC_Labs.pdf  Financial_Report_for_ABC_Labs.txt
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/segundoparcial/redactiongone]
└─$ cat Financial_Report_for_ABC_Labs.txt | grep pico                   
picoCTF{C4n_Y0u_S33_m3_fully}

```
usando la herramienta pdftotext podemos quitar el remarcado y poder ver la informacion que hay dentro

---
### NOTAS ADICCIONALES

---
### REFERENCIAS
