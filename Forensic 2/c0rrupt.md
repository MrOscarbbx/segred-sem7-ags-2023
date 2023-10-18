----
### OBJETIVO 
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.

---
### SOLUCION

En resumidas cuentas podemos ver que el archivo tiene algunos valores que no corresponden a un archivo png, asi que con la ayuda de un editor hexa y la documentacion de los png, podemos corregir los valores y asi reparar el archivo.
``` bash
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ file mystery    
mystery: data
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ xxd mystery | head
00000000: 8965 4e34 0d0a b0aa 0000 000d 4322 4452  .eN4........C"DR
00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..
00000020: 7800 0000 0173 5247 4200 aece 1ce9 0000  x....sRGB.......
00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...
00000040: 0009 7048 5973 aa00 1625 0000 1625 0149  ..pHYs...%...%.I
00000050: 5224 f0aa aaff a5ab 4445 5478 5eec bd3f  R$......DETx^..?
00000060: 8e64 cd71 bd2d 8b20 2080 9041 8302 08d0  .d.q.-.  ..A....
00000070: f9ed 40a0 f36e 407b 9023 8f1e d720 8b3e  ..@..n@{.#... .>
00000080: b7c1 0d70 0374 b503 ae41 6bf8 bea8 fbdc  ...p.t...Ak.....
00000090: 3e7d 2a22 336f de5b 55dd 3d3d f920 9188  >}*"3o.[U.==. ..
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ hexeditor mystery    
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ hexeditor mystery 
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ file mystery
mystery: data
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ xxd mystery | head  
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4322 4452  .PNG........C"DR
00000010: 0000 066a 0000 0447 0802 0000 007c 8bab  ...j...G.....|..
00000020: 7800 0000 0173 5247 4200 aece 1ce9 0000  x....sRGB.......
00000030: 0004 6741 4d41 0000 b18f 0bfc 6105 0000  ..gAMA......a...
00000040: 0009 7048 5973 aa00 1625 0000 1625 0149  ..pHYs...%...%.I
00000050: 5224 f0aa aaff a5ab 4445 5478 5eec bd3f  R$......DETx^..?
00000060: 8e64 cd71 bd2d 8b20 2080 9041 8302 08d0  .d.q.-.  ..A....
00000070: f9ed 40a0 f36e 407b 9023 8f1e d720 8b3e  ..@..n@{.#... .>
00000080: b7c1 0d70 0374 b503 ae41 6bf8 bea8 fbdc  ...p.t...Ak.....
00000090: 3e7d 2a22 336f de5b 55dd 3d3d f920 9188  >}*"3o.[U.==. ..
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ mv mystery mystery.png
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ open mystery.png 
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ ** Message: 01:57:15.944: Could not open file 'file:///home/kali/Picoctf/forense/mystery.png': Unsupported mime type
mv mystery.png  mystery
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ hexeditor mystery      
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ file mystery           
mystery: PNG image data, 1642 x 1095, 8-bit/color RGB, non-interlaced
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ mv mystery mystery.png 
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ open mystery.png       
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ sudo apt install pngcheck          
[sudo] password for kali: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libavutil57 libcodec2-1.0 libplacebo208 libpostproc56 libswscale6
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed:
  pngcheck
0 upgraded, 1 newly installed, 0 to remove and 1109 not upgraded.
Need to get 68.6 kB of archives.
After this operation, 208 kB of additional disk space will be used.
Get:1 http://kali.download/kali kali-rolling/main amd64 pngcheck amd64 3.0.3-3 [68.6 kB]
Fetched 68.6 kB in 1s (88.9 kB/s)
Selecting previously unselected package pngcheck.
(Reading database ... 428736 files and directories currently installed.)
Preparing to unpack .../pngcheck_3.0.3-3_amd64.deb ...
Unpacking pngcheck (3.0.3-3) ...
Setting up pngcheck (3.0.3-3) ...
Processing triggers for man-db (2.11.2-2) ...
Processing triggers for kali-menu (2023.2.3) ...
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ pngcheck mystery.png 
mystery.png  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)
ERROR: mystery.png
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ pngcheck -v mystery.png
File: mystery.png (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 2852132389x5669 pixels/meter
  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)
ERRORS DETECTED in mystery.png
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ hexeditor mystery        
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ hexeditor mystery.png 
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ pngcheck -v mystery.png
File: mystery.png (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in mystery.png
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ hexeditor mystery.png  
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ pngcheck -v mystery.png
File: mystery.png (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in mystery.png
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ hexeditor mystery.png  
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ pngcheck -v mystery.png
File: mystery.png (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
  chunk IDAT at offset 0x00057, length 65445
    zlib: deflated, 32K window, fast compression
  chunk IDAT at offset 0x10008, length 65524
  chunk IDAT at offset 0x20008, length 65524
  chunk IDAT at offset 0x30008, length 6304
  chunk IEND at offset 0x318b4, length 0
No errors detected in mystery.png (9 chunks, 96.3% compression).
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ hexeditor mystery.png  
                                                                                 
┌──(kali㉿kali)-[~/Picoctf/forense]
└─$ open mystery.png      
```
Aqui esan los cambios que realizamoe en el archivo:

![[Pasted image 20231018001436.png]]
Y aqui esta la imagen de la bandera:
picoCTF{c0rrupt10n_1847995}
![[mystery.png]]


---
### NOTAS ADICCIONALES
Puede verse la documentacion de los archivs PNG en el link de las referencias.

---
### REFERENCIAS
https://es.wikipedia.org/wiki/Portable_Network_Graphics