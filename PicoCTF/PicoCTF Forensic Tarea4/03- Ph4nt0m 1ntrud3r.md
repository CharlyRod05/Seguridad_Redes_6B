### Ph4nt0m 1ntrud3r
### Descripcion
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/3fe089c41615b9413666bedca922e07bf6ad8894a3dabd2737735143ad2396cf/myNetworkTraffic.pcap) and try to get the flag.
### Solucion 1
Al ver los paquetes note que habia algunos que tenian en el payload un == lo que podria indicar que habia un string codificado ahi, despues vi que todos los que tenian el payload asi tenian su time_relative mayor a 0.003, intente decodificar algunos encontre fragmentos de la bandera, por ultimo los ordene por tiempo de menor a mayor y al decodificar y concatenar en orden aparecio la bandera. para decodificar se uso cyberchef
[From Hex, From Base64 - CyberChef](https://cyberchef.org/#recipe=From_Hex\('Auto'\)From_Base64\('A-Za-z0-9%2B/%3D',true,false\)&input=NjM0NzZjNmE2MjMwNGU1NTUyNjczZDNkCjY1N2E0NjMwNTgzMzYzMzA2Mzc3M2QzZAo2MjZlNTI2NjY0NDc2NzMwNjQ0MTNkM2QKNTg3YTRkMzA2MzMzNmM2NjY0NDEzZDNkCjU5NmQ2ODY2NGU0ODRhNjY0ZjUxM2QzZAo0ZTZhNWE2YjRkNDc0YTZkNTk2NzNkM2QKNjY1MTNkM2Q)
picoCTF{1t_w4snt_th4t_34sy_tbh_4r_966d0bfb} 
### Solucion 2
ya que sabemos  donde esta la informacion con un solo comando que extraiga los datos los ordene y los decodifique podemos obtener la bandera
```
┌──(kali㉿kali)-[~/forensic/phantomIntruder]
└─$ tshark -r myNetworkTraffic.pcap -T fields \
-e frame.time_relative -e tcp.payload \
| awk '$1 >= 0.003 {print $1, $2}' \
| sort -k1 -n \
| awk '{print $2}' \
| while read p; do echo $p | xxd -r -p | base64 -d; done
picoCTF{1t_w4snt_th4t_34sy_tbh_4r_966d0bfb}  
```
### Notas adicionales

### Referencias

[From Hex, From Base64 - CyberChef](https://cyberchef.org/#recipe=From_Hex\('Auto'\)From_Base64\('A-Za-z0-9%2B/%3D',true,false\)&input=NjM0NzZjNmE2MjMwNGU1NTUyNjczZDNkCjY1N2E0NjMwNTgzMzYzMzA2Mzc3M2QzZAo2MjZlNTI2NjY0NDc2NzMwNjQ0MTNkM2QKNTg3YTRkMzA2MzMzNmM2NjY0NDEzZDNkCjU5NmQ2ODY2NGU0ODRhNjY0ZjUxM2QzZAo0ZTZhNWE2YjRkNDc0YTZkNTk2NzNkM2QKNjY1MTNkM2Q)