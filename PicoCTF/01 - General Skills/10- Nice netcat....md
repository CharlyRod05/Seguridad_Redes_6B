### Nice netcat...

### Descripcion
There is a nice program that you can talk to by using this command in a shell:

Additional details will be available after launching your challenge instance.

$ nc wily-courier.picoctf.net 55317, but it doesn't speak English...
### Solucion
```
CharlyRod-picoctf@webshell:~$ nc wily-courier.picoctf.net 55317
112 105 99 111 67 84 70 123 103 48 48 100 95 107 49 116 116 121 33 95 110 49 99 51 
95 107 49 116 116 121 33 95 102 55 97 54 101 125 10 
```
picoCTF{g00d_k1tty!_n1c3_k1tty!_f7a6e}

[From Charcode - CyberChef](https://cyberchef.org/#recipe=From_Charcode\('Space',10\)&input=MTEyIA0KMTA1IA0KOTkgDQoxMTEgDQo2NyANCjg0IA0KNzAgDQoxMjMgDQoxMDMgDQo0OCANCjQ4IA0KMTAwIA0KOTUgDQoxMDcgDQo0OSANCjExNiANCjExNiANCjEyMSANCjMzIA0KOTUgDQoxMTAgDQo0OSANCjk5IA0KNTEgDQo5NSANCjEwNyANCjQ5IA0KMTE2IA0KMTE2IA0KMTIxIA0KMzMgDQo5NSANCjEwMiANCjU1IA0KOTcgDQo1NCANCjEwMSANCjEyNSANCjEw)
### Notas adicionales
Se utilizo cyberchef pa decodificar ascii

Se puede abrir el archivo en python utilizando open y .read() y despues usar un ciclo para convertir cada caracter e imprimirlo con chr.
### Referencias