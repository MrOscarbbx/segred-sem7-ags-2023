----
### OBJETIVO 
I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check...

Additional details will be available after launching your challenge instance.

---
### SOLUCION
Analizando el codigo que se nos da nos podemos dar cuenta que se esta generando una cadena de caracteres de manera aleatorio, y lo codifica, lo que no conocemos son los numeros primos que se necesitan para poder codificarlo
```python
from Crypto.Util.number import getPrime, inverse, bytes_to_long
from string import ascii_letters, digits
from random import choice

pride = "".join(choice(ascii_letters + digits) for _ in range(16))
gluttony = getPrime(128)
greed = getPrime(128)
lust = gluttony * greed
sloth = 65537
envy = inverse(sloth, (gluttony - 1) * (greed - 1))

anger = pow(bytes_to_long(pride.encode()), sloth, lust)

print(f"{anger = }")
print(f"{envy = }")

print("vainglory?")
vainglory = input("> ").strip()

if vainglory == pride:
    print("Conquered!")
    with open("/challenge/flag.txt") as f:
        print(f.read())
else:
    print("Hubris!")
```

asi que tenemos que buscar los dos numeros primos que se utilizan, asi que podemos usar un script que descubra los dos numeros y decodifique asi el texto
```python
from Crypto.Util.number import isPrime, long_to_bytes 
from string import ascii_letters, digits 
from itertools import combinations 
from sympy import divisors 
from math import log2 
anger = int(input("anger = ")) 
envy = int(input("envy = ")) 
sloth = 65537 
ds = divisors(envy * sloth - 1) 
primes = [x + 1 for x in ds if isPrime(x + 1)] 
correct_size_primes = [x for x in primes if log2(x) // 1 == 127]
valid_plaintexts = [] charset = ascii_letters + digits 
for p, q in combinations(correct_size_primes, 2): 
	try: s = long_to_bytes(pow(anger, envy, p * q)).decode("ascii") 
		if all([c in charset for c in s]): 
			valid_plaintexts.append(s) except Exception: continue print(valid_plaintexts)
```

```bash
┌──(kali㉿kali)-[~/Picoctf/tercerp]
└─$ python solucion.py
anger = 79045688394924724978101584289818820635049240574161222634381571856272285891083
envy = 12742854954622827490575990861638166544238993677870154283292783053685937503073
['g8ppa9V9zQHd7jmG']

```

```bash
┌──(kali㉿kali)-[~]
└─$ nc saturn.picoctf.net 63915
anger = 79045688394924724978101584289818820635049240574161222634381571856272285891083
envy = 12742854954622827490575990861638166544238993677870154283292783053685937503073
vainglory?
> g8ppa9V9zQHd7jmG
g8ppa9V9zQHd7jmG
Conquered!
picoCTF{7h053_51n5_4r3_n0_m0r3_3858bd66}
                                         
```
---
### NOTAS ADICCIONALES

---
### REFERENCIAS
