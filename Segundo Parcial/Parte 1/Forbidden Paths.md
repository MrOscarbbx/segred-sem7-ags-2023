----
### OBJETIVO 
Can you get the flag?Here's the [website](http://saturn.picoctf.net:58179/).We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?

---
### SOLUCION
Si tenemos en cuenta que la pagina se encuentra en la path "/usr/share/nginx/html/" y la bandera esta en "/flag.txt", entonces usando .. podemos regresar al directorio principal, ta 
![[Pasted image 20231023181047.png]]
![[Pasted image 20231023181417.png]]
picoCTF{7h3_p47h_70_5ucc355_6db46514}

---
### NOTAS ADICCIONALES

---
### REFERENCIAS
