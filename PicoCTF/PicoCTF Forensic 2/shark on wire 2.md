### shark on wire 2
### Descripcion
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/ca7e8f9bb6b060dd724f90e3243aa3e36fc0d98c9b421cef0e860d1ff75f9ef0/capture.pcap). Recover the flag.
### Solucion
Al revisar los streams udp vemos un begin y un end en los stream 32 y 60.
ahi notamos que ambos van al puerto 22 por lo que filtramos todos los paquetes que van al puerto 22

al analizar los paquetes vemos que todos vienen de puertos 5### con numeros muy parecidos y que parecen seguir un patron

Al restar 5000 a los numeros de puerto de entrada los valores corresponden con el ascii de la bandera

usando scapy y el siguiente script de python desciframos la bandera
```
from scapy.all import *

packets = rdpcap('capture.pcap')

flag=''

for p in packets:
    if UDP in p and p[UDP].dport == 22:
        if p[UDP].sport > 5000:
            flag+=chr(p[UDP].sport - 5000)

print(flag)
```

picoCTF{p1LLf3r3d_data_v1a_st3g0}

### Notas adicionales

### Referencias
