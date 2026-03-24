### Disk, disk, sleuth!
### Descripcion
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image. [dds1-alpine.flag.img.gz](https://challenge-files.picoctf.net/c_wily_courier/8643b47c3c19e52e891a4684258e1d1cbb65094afa9cf81317b563004a739653/dds1-alpine.flag.img.gz)
### Solucion
```
┌──(kali㉿kali)-[~/forensic/diskdisk]
└─$ ls
dds1-alpine.flag.img.gz
                                                                             
┌──(kali㉿kali)-[~/forensic/diskdisk]
└─$ gzip -d dds1-alpine.flag.img.gz 
                                                                             
┌──(kali㉿kali)-[~/forensic/diskdisk]
└─$ ls
dds1-alpine.flag.img
                                                                             
┌──(kali㉿kali)-[~/forensic/diskdisk]
└─$ srch_strings dds1-alpine.flag.img | grep pico 
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_5e56e786}

```

picoCTF{f0r3ns1c4t0r_n30phyt3_5e56e786}
### Notas adicionales

### Referencias