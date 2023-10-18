----
### OBJETIVO 
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

---
### SOLUCION
Al navegar por el stream UDP de la captura de paquetes podemos encontrar un inicio en el stream numero 32 y un fin el stream numero 60
![[Pasted image 20231018011012.png]]
![[Pasted image 20231018012333.png]]
Podemos ver que ambas capturas son recibidas en el puerto 22
![[Pasted image 20231018012417.png]]
Filtrando las capturas que solo esten en el puerto 22 podemos encontrar un patron en los puestos de salida, que se tratan de un cadigo para convertir de ascii a string:
![[Pasted image 20231018011336.png]]
Usando la siguiente codigo de python podemos sacar los valores de los puertos sin problemas:
``` python                                
from scapy.all import *


packets = rdpcap('capture.pcap.1')

flag = ''

for p in  packets:
        if UDP in p and p[UDP].dport == 22:
                if p[UDP].sport > 5000:
                        flag += chr(p[UDP].sport - 5000)

print(flag)


```



``` bash
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ nano expcap.py  
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ python expcap.py
picoCTF{p1LLf3r3d_data_v1a_st3g0}

```


---
### NOTAS ADICCIONALES
Scapy is a powerful interactive packet manipulation library written in Python. Scapy is able to forge or decode packets of a wide number of protocols, send them on the wire, capture them, match requests and replies, and much more.

---
### REFERENCIAS
https://scapy.net/