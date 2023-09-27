

## Solucion
	C:\Users\mrosc> ssh ctf-player@venus.picoctf.net -p 57924 
		The authenticity of host '[venus.picoctf.net]:57924 ([3.131.124.143]:57924)' can't be established.
		ECDSA key fingerprint is SHA256:NrQkIxNEQQho/GA7jE0WlIa7Jh4VF9sAvC5awkbuj1Q.
		Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
		Warning: Permanently added '[venus.picoctf.net]:57924,[3.131.124.143]:57924' (ECDSA) to the list of known hosts.
		ctf-player@venus.picoctf.net's password:
		Welcome to Ubuntu 18.04.5 LTS (GNU/Linux 5.4.0-1041-aws x86_64)
		Documentation:  https://help.ubuntu.com                                            * Management:     https://landscape.canonical.com                                  * Support:        https://ubuntu.com/advantage                                    This system has been minimized by removing packages and content that are           not required on a system that users do not log into.                               To restore this content, you can run the 'unminimize' command.                     Last login: Mon Sep 25 14:21:50 2023 from 127.0.0.1                                ctf-player@pico-chall$ ls                                                          1of3.flag.txt  instructions-to-2of3.txt                                            ctf-player@pico-chall$ cat 1of3.flag.txt                                           picoCTF{xxsh_                                                                      ctf-player@pico-chall$ cat instructions-to-2of3.txt                                Next, go to the root of all things, more succinctly `/`                            ctf-player@pico-chall$ cd /                                                        ctf-player@pico-chall$ ls                                                         2of3.flag.txt  boot  etc   instructions-to-3of3.txt  lib64  mnt  proc  run   srv  tmp  var  bin  dev   home  lib media  opt  root  sbin  sys  usr
		ctf-player@pico-chall$ cat 2of3.flag.txt                                           0ut_0f_\/\/4t3r_
		ctf-player@pico-chall$ cat instructions-to-3of3.txt                                Lastly, ctf-player, go home... more succinctly `~`                                 ctf-player@pico-chall$ cd ~                                                        ctf-player@pico-chall$ ls                                                          3of3.flag.txt  drop-in                                                             ctf-player@pico-chall$ cat 3of3.flag.txt                                           5190b070}                                                                          ctf-player@pico-chall$ 

	picoCTF{xxsh_0ut_0f_\/\/4t3r_5190b070}

Pues nada mas es ir a los directorios que nos dicen jijijij nada mas fuera de lo normal