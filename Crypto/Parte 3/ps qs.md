----
### OBJETIVO 
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/51d68e61bb41207a55f24e753f07c5a3/values)

---
### SOLUCION

``` python
mrioso-picoctf@webshell:~$ ls
README.txt  values
mrioso-picoctf@webshell:~$ cat values 
Decrypt my super sick RSA:
c: 62324783949134119159408816513334912534343517300880137691662780895409992760262021
n: 1280678415822214057864524798453297819181910621573945477544758171055968245116423923
e: 65537mrioso-picoctf@webshell:~$ 
mrioso-picoctf@webshell:~$ python 
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> c = 62324783949134119159408816513334912534343517300880137691662780895409992760262021
>>> n = 1280678415822214057864524798453297819181910621573945477544758171055968245116423923
>>> e = 65537
>>> pow(c,e,n)
676502447953564296700484079859625391048333096541821869759361335641047246931643071
>>> from Crypto.Util.number import long_to_bytes
>>> long_to_bytes(676502447953564296700484079859625391048333096541821869759361335641047246931643071)
b'\x16\xd2c\xa0\x8bT\x94\x1b,\xac\xa4P\xad0?E \x97\xbb\xb6\xdc\xf4\xe0\xcc_\x04\xe8\xaf([8\x16J\xbf'
>>> p = 1899107986527483535344517113948531328331
>>> q = 674357869540600933870145899564746495319033
>>> tn = (p-1) * (q-1)
>>> from gmpy2 import *
>>> inverse(e,tn)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'inverse' is not defined. Did you mean: 'invert'?
>>> from Crypto.Util.number import inverse
>>> inverse(e,tn)
449332735606084960351204406909610297301574728466820933515942864925459265983556193
>>> b = inverse(e,tn)
>>> pow(c,b,n)
13016382529449106065927291425342535437996222135352905256639555654677400177227645
>>> long_to_bytes(13016382529449106065927291425342535437996222135352905256639555654677400177227645)
b'picoCTF{sma11_N_n0_g0od_05012767}'
```

usando una pagina podemos factorizar n para poder sacar p y q
![[Pasted image 20231030222955.png]]


---
### NOTAS ADICCIONALES

``` python
 from Crypto.Util.number import long_to_bytes
 from Crypto.Util.number import inverse
```

---
### REFERENCIAS
http://factordb.com/index.php?query=1280678415822214057864524798453297819181910621573945477544758171055968245116423923