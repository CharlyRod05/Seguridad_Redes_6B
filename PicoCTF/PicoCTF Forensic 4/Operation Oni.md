### Operation Oni
### Descripcion
Download this disk image, find the key and log into the remote machine. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

Additional details will be available after launching your challenge instance.
- [Download disk image](https://artifacts.picoctf.net/c/70/disk.img.gz)
- Remote machine: `ssh -i key_file -p 61178 ctf-player@saturn.picoctf.net`
### Solucion
```
└─$ mmls disk.img                      
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)


┌──(kali㉿kali)-[~/forensic/operationONI]
└─$ fls -o 0000206848 disk.img 470
r/r 2344:    .ash_history
d/d 3916:    .ssh
                                                                             
┌──(kali㉿kali)-[~/forensic/operationONI]
└─$ fls -o 0000206848 disk.img 470 -r
r/r 2344:    .ash_history
d/d 3916:    .ssh
+ r/r 2345:  id_ed25519
+ r/r 2346:  id_ed25519.pub
                                                                             
┌──(kali㉿kali)-[~/forensic/operationONI]
└─$ icat -o 0000206848 disk.img 2345 > key_file  

┌──(kali㉿kali)-[~/forensic/operationONI]
└─$ chmod 600 key_file 
                                                                             
┌──(kali㉿kali)-[~/forensic/operationONI]
└─$ ssh -i key_file -p 61178 ctf-player@saturn.picoctf.net

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt 
picoCTF{k3y_5l3u7h_b5066e83}
```
picoCTF{k3y_5l3u7h_b5066e83}
### Notas adicionales

### Referencias