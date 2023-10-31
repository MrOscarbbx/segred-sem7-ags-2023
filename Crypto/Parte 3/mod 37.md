----
### OBJETIVO 

We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/127/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)


---
### SOLUCION

Nos dan estos numeros 
``` bash
128 322 353 235 336 73 198 332 202 285 57 87 262 221 218 405 335 101 256 227 112 140
```

usando un decodificador de mod 37 nos dan la respuesta

![[Pasted image 20231030223616.png]]

picoCTF{R0UND_N_R0UND_79C18FB3}

---
### NOTAS ADICCIONALES

A modulo cipher uses modular calculus on numbers in order to extract the remainder. The values obtained can then be used as a code/index for another cipher such as [A1Z26](https://www.dcode.fr/letter-number-cipher) or the [ASCII code](https://www.dcode.fr/ascii-code)

---
### REFERENCIAS
https://www.dcode.fr/modulo-cipher?__r=1.239030dab20d7c11ffed25e48c4cfabc