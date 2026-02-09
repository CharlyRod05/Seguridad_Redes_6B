
### Bases

### Descripcion
What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.
### Solucion
### Solucion1- Consola

```
CharlyRod-picoctf@webshell:~$ echo 'bDNhcm5fdGgzX3IwcDM1' | base64 -d
l3arn_th3_r0p35
```

picoCTF{l3arn_th3_r0p35}

### Solucion2- Cyberchef

[From Base64 - CyberChef](https://cyberchef.org/#recipe=From_Base64\('A-Za-z0-9%2B/%3D',true,false\)&input=YkROaGNtNWZkR2d6WDNJd2NETTE)

### Solucion3- python
```
CharlyRod-picoctf@webshell:~$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import base64
>>> base64.b64decode('bDNhcm5fdGgzX3IwcDM1')
b'l3arn_th3_r0p35'
>>> 
```
l3arn_th3_r0p35
### Notas adicionales

### Referencias