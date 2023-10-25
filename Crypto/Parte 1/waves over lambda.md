----
### OBJETIVO 
We made a lot of substitutions to encrypt this. Can you decrypt it? Connect with `nc jupiter.challenges.picoctf.org 43522`.

---
### SOLUCION

Al entrar a el netcat encontramos esta salida
``` bash
-------------------------------------------------------------------------------
neaivdsr ycvc kr qebv txdi - tvcfbcanq_kr_n_ezcv_xdhwud_eithdbavdt
-------------------------------------------------------------------------------
gc gcvc aes hbny hevc syda d fbdvscv et da yebv ebs et ebv rykj skxx gc rdg ycv rkam, dau syca k baucvrseeu tev syc tkvrs skhc gyds gdr hcdas wq d rykj tebaucvkai ka syc rcd.  k hbrs dnmaegxcuic k ydu ydvuxq cqcr se xeem bj gyca syc rcdhca sexu hc ryc gdr rkamkai; tev tveh syc hehcas syds sycq vdsycv jbs hc kase syc weds syda syds k hkiys wc rdku se ie ka, hq ycdvs gdr, dr ks gcvc, ucdu gksyka hc, jdvsxq gksy tvkiys, jdvsxq gksy yevvev et hkau, dau syc syebiysr et gyds gdr qcs wctevc hc.

```

podemos ver que es cifrado por sustitucion asi que entramos a un decodificador para poder decodificarlo con fuerza bruta ya que no tenemos la llave

![[Pasted image 20231024215648.png]]
y listo asi encontramos la llave
frequency_is_c_over_lambda_ogfmaunraf


---
### NOTAS ADICCIONALES
In [cryptography](https://en.wikipedia.org/wiki/Cryptography "Cryptography"), a **substitution cipher** is a method of [encrypting](https://en.wikipedia.org/wiki/Encrypting "Encrypting") in which units of [plaintext](https://en.wikipedia.org/wiki/Plaintext "Plaintext") are replaced with the [ciphertext](https://en.wikipedia.org/wiki/Ciphertext "Ciphertext"), in a defined manner, with the help of a key; the "units" may be single letters (the most common), pairs of letters, triplets of letters, mixtures of the above, and so forth. The receiver deciphers the text by performing the inverse substitution process to extract the original message.

---
### REFERENCIAS
https://en.wikipedia.org/wiki/Substitution_cipher
https://www.guballa.de/substitution-solver