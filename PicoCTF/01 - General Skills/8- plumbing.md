### plumbing

### Descripcion
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?

Additional details will be available after launching your challenge instance.


### Solucion
```
CharlyRod-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 65434 | grep picoCTF
picoCTF{digital_plumb3r_00da27CC}
```

picoCTF{digital_plumb3r_00da27CC}
### Notas adicionales
La respuesta del servidor se puede encadenar a un grep con un | (pipe)
### Referencias