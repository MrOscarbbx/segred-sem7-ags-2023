----
### OBJETIVO 

I found this cipher in an old book. Can you figure out what it says? Connect with `nc jupiter.challenges.picoctf.org 32411`.

---
### SOLUCION

``` bash
mrioso-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 32411 
Encrypted message:
Ne iy nytkwpsznyg nth it mtsztcy vjzprj zfzjy rkhpibj nrkitt ltc tnnygy ysee itd tte cxjltk

Ifrosr tnj noawde uk siyyzre, yse Bnretèwp Cousex mls hjpn xjtnbjytki xatd eisjd

Iz bls lfwskqj azycihzeej yz Brftsk ip Volpnèxj ls oy hay tcimnyarqj dkxnrogpd os 1553 my Mnzvgs Mazytszf Merqlsu ny hox moup Wa inqrg ipl. Ynr. Gotgat Gltzndtg Gplrfdo 

Ltc tnj tmvqpmkseaznzn uk ehox nivmpr g ylbrj ts ltcmki my yqtdosr tnj wocjc hgqq ol fy oxitngwj arusahje fuw ln guaaxjytrd catizm tzxbkw zf vqlckx hizm ceyupcz yz tnj fpvjc hgqqpohzCZK{m311a50_0x_a1rn3x3_h1ah3x7g996649}

Ehk ktryy herq-ooizxetypd jjdcxnatoty ol f aordllvmlbkytc inahkw socjgex, bls sfoe gwzuti 1467 my Rjzn Hfetoxea Gqmexyt.

Tnj Gimjyèrk Htpnjc iy ysexjqoxj dosjeisjd cgqwej yse Gqmexyt Doxn ox Fwbkwei Inahkw.

Tn 1508, Ptsatsps Zwttnjxiax tnbjytki ehk xz-cgqwej ylbaql rkhea (g rltxni ol xsilypd gqahggpty) ysaz bzuri wazjc bk f nroytcgq nosuznkse ol yse Bnretèwp Cousex.

Gplrfdo’y xpcuso butvlky lpvjlrki tn 1555 gx l cuseitzltoty ol yse lncsz. Yse rthex mllbjd ol yse gqahggpty fce tth snnqtki cemzwaxqj, bay ehk fwpnfmezx lnj yse osoed qptzjcs gwp mocpd hd xegsd ol f xnkrznoh vee usrgxp, wnnnh ify bk itfljcety hizm paim noxwpsvtydkse.
```
despues de intentar el rot13 y caesar y no encontrar nada, con vigenere podemos decodificar el texto y encontrar la bandera con la llave "FLAG"
![[Pasted image 20231024214010.png]]

picoCTF{b311a50_0r_v1gn3r3_c1ph3r7b996649}

---
### NOTAS ADICCIONALES

---
### REFERENCIAS
https://gchq.github.io/CyberChef/#recipe=Vigen%C3%A8re_Decode('flag')&input=TmUgaXkgbnl0a3dwc3pueWcgbnRoIGl0IG10c3p0Y3kgdmp6cHJqIHpmemp5IHJraHBpYmogbnJraXR0IGx0YyB0bm55Z3kgeXNlZSBpdGQgdHRlIGN4amx0awoKSWZyb3NyIHRuaiBub2F3ZGUgdWsgc2l5eXpyZSwgeXNlIEJucmV0w6h3cCBDb3VzZXggbWxzIGhqcG4geGp0bmJqeXRraSB4YXRkIGVpc2pkCgpJeiBibHMgbGZ3c2txaiBhenljaWh6ZWVqIHl6IEJyZnRzayBpcCBWb2xwbsOoeGogbHMgb3kgaGF5IHRjaW1ueWFycWogZGt4bnJvZ3BkIG9zIDE1NTMgbXkgTW56dmdzIE1henl0c3pmIE1lcnFsc3UgbnkgaG94IG1vdXAgV2EgaW5xcmcgaXBsLiBZbnIuIEdvdGdhdCBHbHR6bmR0ZyBHcGxyZmRvIAoKTHRjIHRuaiB0bXZxcG1rc2Vhem56biB1ayBlaG94IG5pdm1wciBnIHlsYnJqIHRzIGx0Y21raSBteSB5cXRkb3NyIHRuaiB3b2NqYyBoZ3FxIG9sIGZ5IG94aXRuZ3dqIGFydXNhaGplIGZ1dyBsbiBndWFheGp5dHJkIGNhdGl6bSB0enhia3cgemYgdnFsY2t4IGhpem0gY2V5dXBjeiB5eiB0bmogZnB2amMgaGdxcXBvaHpDWkt7bTMxMWE1MF8weF9hMXJuM3gzX2gxYWgzeDdnOTk2NjQ5fQoKRWhrIGt0cnl5IGhlcnEtb29penhldHlwZCBqamRjeG5hdG90eSBvbCBmIGFvcmRsbHZtbGJreXRjIGluYWhrdyBzb2NqZ2V4LCBibHMgc2ZvZSBnd3p1dGkgMTQ2NyBteSBSanpuIEhmZXRveGVhIEdxbWV4eXQuCgpUbmogR2ltannDqHJrIEh0cG5qYyBpeSB5c2V4anFveGogZG9zamVpc2pkIGNncXdlaiB5c2UgR3FtZXh5dCBEb3huIG94IEZ3Ymt3ZWkgSW5haGt3LgoKVG4gMTUwOCwgUHRzYXRzcHMgWnd0dG5qeGlheCB0bmJqeXRraSBlaGsgeHotY2dxd2VqIHlsYmFxbCBya2hlYSAoZyBybHR4bmkgb2wgeHNpbHlwZCBncWFoZ2dwdHkpIHlzYXogYnp1cmkgd2F6amMgYmsgZiBucm95dGNncSBub3N1em5rc2Ugb2wgeXNlIEJucmV0w6h3cCBDb3VzZXguCgpHcGxyZmRv4oCZeSB4cGN1c28gYnV0dmxreSBscHZqbHJraSB0biAxNTU1IGd4IGwgY3VzZWl0emx0b3R5IG9sIHlzZSBsbmNzei4gWXNlIHJ0aGV4IG1sbGJqZCBvbCB5c2UgZ3FhaGdncHR5IGZjZSB0dGggc25ucXRraSBjZW16d2F4cWosIGJheSBlaGsgZndwbmZtZXp4IGxuaiB5c2Ugb3NvZWQgcXB0empjcyBnd3AgbW9jcGQgaGQgeGVnc2Qgb2wgZiB4bmtyem5vaCB2ZWUgdXNyZ3hwLCB3bm5uaCBpZnkgYmsgaXRmbGpjZXR5IGhpem0gcGFpbSBub3h3cHN2dHlka3NlLg
