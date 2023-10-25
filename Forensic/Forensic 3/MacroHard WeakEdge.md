---
---
### SOLUCION
Empezamos viendo que contiene el archivo:
![[Pasted image 20231023000315.png]]
Como podemos ver no tienen nada asi que procedemos a descomprimirlo para ver que documentos tiene dentro:
``` bash
┌──(kali㉿kali)-[~/Picoctf/forense/macrohard]
└─$ ls
'[Content_Types].xml'   docProps  'Forensics is fun.pptm'   ppt   _rels
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense/macrohard]
└─$ code .   
```
Para poder visualizar los documentos de manera mas sencilla podemos utilizar Vscode:
![[Pasted image 20231023000939.png]]
Despues de encontrar esa clave escondida usando el bash procedemos a desencriptarla:
``` bash                                                                         
┌──(kali㉿kali)-[~/Picoctf/forense/macrohard]
└─$ echo "Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q" | tr -d " "
ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQ
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense/macrohard]
└─$ 
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense/macrohard]
└─$ echo "Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q" | tr -d " " | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}
```


---
### NOTAS ADICCIONALES

---
### REFERENCIAS
