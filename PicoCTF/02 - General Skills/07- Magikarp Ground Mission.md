### Magikarp Ground Mission
### Descripcion
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin.

Additional details will be available after launching your challenge instance.

Login via `ssh` as `ctf-player` with the password, `8c606eb1` on the host `wily-courier.picoctf.net` and port `49853`.
### Solucion
```
CharlyRod-picoctf@webshell:~$ ssh ctf-player@wily-courier.picoctf.net -p49853
The authenticity of host '[wily-courier.picoctf.net]:49853 ([18.189.99.27]:49853)' can't be established.
ED25519 key fingerprint is SHA256:ErlUUvYlrAxfSW1tIdzfOnGTBSr5OFkZvz0nMN4Vodw.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[wily-courier.picoctf.net]:49853' (ED25519) to the list of known hosts.
ctf-player@wily-courier.picoctf.net's password: 
Permission denied, please try again.
ctf-player@wily-courier.picoctf.net's password: 
Permission denied, please try again.
ctf-player@wily-courier.picoctf.net's password: 
ctf-player@wily-courier.picoctf.net: Permission denied (publickey,password).
CharlyRod-picoctf@webshell:~$ ssh ctf-player@wily-courier.picoctf.net -p49853
ctf-player@wily-courier.picoctf.net's password: 
Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 6.14.0-1012-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat instructions-to-2of3.txt 
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cat     
1of3.flag.txt             instructions-to-2of3.txt  
ctf-player@pico-chall$ cat 
1of3.flag.txt             instructions-to-2of3.txt  
ctf-player@pico-chall$ cat 1of3.flag.txt 
picoCTF{xxsh_
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  challenge  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_//4t3r_
ctf-player@pico-chall$ cat instructions-to-3of3.txt 
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd ~                                                                                                                               
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt 
0b24fc4f}
```

picoCTF{xxsh_0ut_0f_//4t3r_0b24fc4f}
### Notas adicionales

### Referencias