### Wave a flag
### Descripcion
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...[warm](https://challenge-files.picoctf.net/c_wily_courier/70013ed41d4cfe2bb48628471dac6fc12238b5dbe164301ae3b4e35277b1e80b/warm)

### Solucion
```
CharlyRod-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/70013ed41d4cfe2bb48628471dac6fc12238b5dbe164301ae3b4e35277b1e80b/warm
--2026-02-11 14:16:38--  https://challenge-files.picoctf.net/c_wily_courier/70013ed41d4cfe2bb48628471dac6fc12238b5dbe164301ae3b4e35277b1e80b/warm
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.40, 3.160.5.95, 3.160.5.18, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19312 (19K) [application/octet-stream]
Saving to: 'warm'

warm                                                       100%[=======================================================================================================================================>]  18.86K  --.-KB/s    in 0.008s  

2026-02-11 14:16:38 (2.43 MB/s) - 'warm' saved [19312/19312]

CharlyRod-picoctf@webshell:~$ ls
README.txt  file  file.1  flag  warm
CharlyRod-picoctf@webshell:~$ file warm
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=9e46ec8729d2f2aa8ffc4b1cdc058081bddcfe67, for GNU/Linux 3.2.0, with debug_info, not stripped
CharlyRod-picoctf@webshell:~$ ./warm
-bash: ./warm: Permission denied
CharlyRod-picoctf@webshell:~$ chmod +x warm
CharlyRod-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
CharlyRod-picoctf@webshell:~$ warm -h
-bash: warm: command not found
CharlyRod-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
CharlyRod-picoctf@webshell:~$ 
```
picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}

### Notas adicionales
se puede solucionar con strings porque en alguna parte del codigo esta la propia bandera
### Referencias