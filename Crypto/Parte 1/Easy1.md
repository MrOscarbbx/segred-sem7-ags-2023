----
### OBJETIVO 
The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help `UFJKXQZQUNB` with the key of `SOLVECRYPTO`. Can you use this [table](https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt) to solve it?.

---
### SOLUCION

Al abrir la tabla nos muestra una tabla para desencriptar la clave
![[Pasted image 20231024205100.png]]
Este tipo de codificacion se llama Vigenere, lo podemos hacer a mano tomando los caracteres de la llave y tomando el caracter que se encuentra en el encabezado del caracter de la llave cifrada, o podemos usar cyberchef:
![[Pasted image 20231024204829.png]]
y asi encontramos la bandera de este reto
picoCTF{CRYPTOISFUN}

---
### NOTAS ADICCIONALES

The **Vigenère cipher** (French pronunciation: [[viʒnɛːʁ]](https://en.wikipedia.org/wiki/Help:IPA/French "Help:IPA/French")) is a method of [encrypting](https://en.wikipedia.org/wiki/Encryption "Encryption") [alphabetic](https://en.wikipedia.org/wiki/Alphabetic "Alphabetic") text where each letter of the [plaintext](https://en.wikipedia.org/wiki/Plaintext "Plaintext") is encoded with a different [Caesar cipher](https://en.wikipedia.org/wiki/Caesar_cipher "Caesar cipher"), whose increment is determined by the corresponding letter of another text, the [key](https://en.wikipedia.org/wiki/Key_(cryptography) "Key (cryptography)").

---
### REFERENCIAS
https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher