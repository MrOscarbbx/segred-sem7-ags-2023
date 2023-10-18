----
### OBJETIVO 
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/74274b96fe966126a1953c80762af80d/whitepages.txt) is all blank!

---
### SOLUCION	

	┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ nano exp.py
	
``` python
from pwn import *

file = open('whitepages.txt','rb')
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83',b'0')
data = data.replace(b'\x20',b'1')
data = data.decode('ascii')
data = unbits(data)
print(data)
```

	┌──(kali㉿kali)-[~/Picoctf/forense]
	└─$ python exp.py
	b'\n\t\tpicoCTF\n\n\t\tSEE PUBLIC RECORDS & BACKGROUND REPORT\n\t\t5000 Forbes Ave, Pittsburgh, PA 15213\n\t\tpicoCTF{not_all_spaces_are_created_equal_c54f27cd05c2189f8147cc6f5deb2e56}\n\t\t'

---
### NOTAS ADICCIONALES

---
### REFERENCIAS
