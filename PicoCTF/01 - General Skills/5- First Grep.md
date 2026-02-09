
### First Grep

### Descripcion
Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way.The flag is in this [file](https://challenge-files.picoctf.net/c_fickle_tempest/2e9bfa4e1d90ac25a999fefdfb4feb8a2ff4eb73e4c61af4889a3762687ada01/file).
### Solucion
```
CharlyRod-picoctf@webshell:~$ cat file | grep "picoCTF"

CharlyRod-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_fickle_tempest/2e9bfa4e1d90ac25a999fefdfb4feb8a2ff4eb73e4c61af4889a3762687ada01/file
```

picoCTF{grep_is_good_to_find_things_29f42460}
### Notas adicionales
wget para descargar archivo en consola

grep marca en rojo el lugar donde encuentra la cadena
### Referencias
