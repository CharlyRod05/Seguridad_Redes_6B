### SUDO MAKE ME A SANDWICH
### Descripcion
Can you read the flag? I think you can!`ssh -p 59645 ctf-player@green-hill.picoctf.net` using password `f7e73aca`
### Solucion
Se utiliza sudo -i para obtener los comandos que no requieren contraseña
emacs no pide contraseña para ejecutarse como sudo y desde el editor se ejecuta un shell como root y simplemente usamos un cat

```
root@challenge:/home/ctf-player# cat flag.txt 
picoCTF{ju57_5ud0_17_9418380d}
```

### Notas adicionales

### Referencias

