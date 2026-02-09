### what's a netcat


### Descripcion
Additional details will be available after launching your challenge instance.

Using netcat (nc) is going to be pretty important. Can you connect to fickle-tempest.picoctf.net at port 60253 to get the flag?
### Solucion
```
CharlyRod-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 60253 
You're on your way to becoming the net cat master
picoCTF{nEtCat_Mast3ry_aC66D475}
```
picoCTF{nEtCat_Mast3ry_aC66D475}
### Notas adicionales
**Netcat** es una [herramienta de red](https://es.wikipedia.org/w/index.php?title=Herramienta_de_red&action=edit&redlink=1 "Herramienta de red (aún no redactado)") que permite a través de intérprete de comandos y con una sintaxis sencilla abrir puertos TCP/UDP en un HOST (quedando netcat a la escucha), asociar una shell a un puerto en concreto (para conectarse por ejemplo a [MS-DOS](https://es.wikipedia.org/wiki/MS-DOS "MS-DOS") o al intérprete bash de Linux remotamente) y forzar conexiones UDP/TCP (útil por ejemplo para realizar rastreos de puertos o realizar transferencias de archivos bit a bit entre dos equipos). Fue originalmente desarrollada por Hobbit en 1996 y liberada bajo una [licencia](https://es.wikipedia.org/wiki/Licencia_de_software "Licencia de software") de [software libre](https://es.wikipedia.org/wiki/Software_libre "Software libre") permisiva (no [copyleft](https://es.wikipedia.org/wiki/Copyleft "Copyleft"), similar a BSD, MIT) para UNIX. Posteriormente fue portada a [Windows](https://es.wikipedia.org/wiki/Windows "Windows") y [Mac OS X](https://es.wikipedia.org/wiki/Mac_OS_X "Mac OS X") entre otras plataformas. Existen muchos [forks](https://es.wikipedia.org/wiki/Bifurcaci%C3%B3n_\(desarrollo_de_software\) "Bifurcación (desarrollo de software)") de esta herramienta que añaden características nuevas como GNU Netcat o Cryptcat.

Entre sus múltiples aplicaciones, es frecuente la depuración de aplicaciones de red. También es utilizada a menudo para abrir puertas traseras en un sistema.
### Referencias
[Netcat - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/Netcat)