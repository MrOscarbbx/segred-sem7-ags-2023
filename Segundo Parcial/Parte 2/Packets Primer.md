----
### OBJETIVO 

Download the packet capture file and use packet analysis software to find the flag.
- [Download packet capture](https://artifacts.picoctf.net/c/194/network-dump.flag.pcap)
---
### SOLUCION
Entrando a el wireshark lo encontramos en la entrada con un vaso de galletas y un vaso de leche, solo hay que quitarle los espacios
![[Pasted image 20231023231032.png]]
``` bash
┌──(kali㉿kali)-[~]
└─$ echo "p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ c e c c a a 7 f }" | tr -d " "
picoCTF{p4ck37_5h4rk_ceccaa7f}

```
y listo

---
### NOTAS ADICCIONALES

---
### REFERENCIAS
