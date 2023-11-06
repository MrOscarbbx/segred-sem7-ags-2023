----
### OBJETIVO 
In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: [VaultDoor5.java](https://jupiter.challenges.picoctf.org/static/0a53bf0deaba6919f98d8550c35aa253/VaultDoor5.java)

---
### SOLUCION
Para poder decodificar los codigos, tenemos que decodificar primero de base64 y despues de el URL 
![[Pasted image 20231105224706.png]]

---
### NOTAS ADICCIONALES
URL encoding, also known as "percent-encoding", is a mechanism for encoding information in a Uniform Resource Identifier (URI). Although it is known as URL encoding it is, in fact, used more generally within the main Uniform Resource Identifier (URI) set, which includes both Uniform Resource Locator (URL) and Uniform Resource Name (URN). As such it is also used in the preparation of data of the "application/x-www-form-urlencoded" media type, as is often employed in the submission of HTML form data in HTTP requests.

---
### REFERENCIAS
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)URL_Decode()&input=SlRZekpUTXdKVFpsSlRjMkpUTXpKVGN5SlRjMEpUTXhKVFpsSlRZM0pUVm1KVFkySlRjeUpUTXdKVFprSlRWbUpUWXlKVFl4SlRNMUpUWTFKVFZtSlRNMkpUTTBKVFZtSlRNd0pUWXlKVE01SlRNMUpUTTNKVFl6SlRNMEpUWTIi

https://www.urlencoder.org/