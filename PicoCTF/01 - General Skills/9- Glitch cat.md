### Glitch cat

### Descripcion
Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance.
### Solucion
```
CharlyRod-picoctf@webshell:~$ nc saturn.picoctf.net 55803
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
^C
CharlyRod-picoctf@webshell:~$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
'picoCTF{gl17ch_m3_n07_9c42a45d}'
```
picoCTF{gl17ch_m3_n07_9c42a45d}
### Notas adicionales
La bandera esta escrita en forma de codigo de python y la terminal de python retorna la bandera completa
### Referencias
