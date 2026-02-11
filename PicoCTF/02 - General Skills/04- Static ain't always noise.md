### Static ain't always noise

### Descripcion
Can you look at the data in this binary? The bash script might help![static](https://challenge-files.picoctf.net/c_wily_courier/418e2775a501eaabeb99a96c5c467a83539369fe9649e8234644250cfb72d717/static), [ltdis.sh](https://challenge-files.picoctf.net/c_wily_courier/418e2775a501eaabeb99a96c5c467a83539369fe9649e8234644250cfb72d717/ltdis.sh)
### Solucion
```
CharlyRod-picoctf@webshell:~$ ./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
CharlyRod-picoctf@webshell:~$ ls
README.txt  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt

CharlyRod-picoctf@webshell:~$ cat static.ltdis.strings.txt | grep pico
   3020 picoCTF{d15a5m_t34s3r_20335e41}
```
picoCTF{d15a5m_t34s3r_20335e41}

### Notas adicionales

### Referencias
