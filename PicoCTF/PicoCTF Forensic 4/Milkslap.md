### Milkslap
### Descripcion
http://wily-courier.picoctf.net:62044/
### Solucion
se entra al código fuente del sitio y se descarga la imagen, despues zsteg con buffer aumentado:

```
┌──(kali㉿kali)-[~/forensic/Milkslap]
└─$ RUBY_THREAD_VM_STACK_SIZE=5242880 zsteg -a concat_v.png

```
picoCTF{imag3_m4n1pul4t10n_sl4p5}
### Notas adicionales

### Referencias