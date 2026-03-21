### c0rrupt

### Descripcion
We found this [file](https://challenge-files.picoctf.net/c_fickle_tempest/87bdc8ce30b177d033b3d68bca4647950bb07304032861baa912ebe08701d355/mystery). Recover the flag.
### Solucion
Se debe reconstruir el archivo siguiendo la estructura de un png

La cabecera no corresponde con la de un png asi que con hexeditor se cambia por `89 50 4E 47 0D 0A 1A 0A`

el chunk ihdr no tiene el nombre bien `43 22 44 52` por `49 48 44 52`

utilizando pngcheck podemos ver que chunks tienen problema

corregimos `pHys`, cambiamos `aa 00 16 25 00 00 16 25` por `00 00 16 25 00 00 16 25`
El tamaño de IDAT no tiene sentido y su nombre tambien esta mal por lo que se corrigen
cambiamos `AA AA FF A5` por `00 00 FF A5`
cambiamos `AB 44 45 54` por `49 44 41 54`
al abrir el archivo esta la bandera
### Notas adicionales

### Referencias
