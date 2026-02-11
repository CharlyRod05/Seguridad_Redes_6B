### Tab, Tab, Attack

### Descripcion
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames.[Addadshashanammu.zip](https://challenge-files.picoctf.net/c_wily_courier/730d9106a6ce1d52c6463b90937ec89f5eb661388954fbd15cfa0c8a2eec012f/Addadshashanammu.zip)
### Solucion
```
CharlyRod-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/730d9106a6ce1d52c6463b90937ec89f5eb661388954fbd15cfa0c8a2eec012f/Addadshashanammu.zip
--2026-02-11 14:40:39--  https://challenge-files.picoctf.net/c_wily_courier/730d9106a6ce1d52c6463b90937ec89f5eb661388954fbd15cfa0c8a2eec012f/Addadshashanammu.zip
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.64, 3.160.5.40, 3.160.5.18, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 5166 (5.0K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip'

Addadshashanammu.zip                                       100%[=======================================================================================================================================>]   5.04K  --.-KB/s    in 0.001s  

2026-02-11 14:40:39 (4.33 MB/s) - 'Addadshashanammu.zip' saved [5166/5166]

CharlyRod-picoctf@webshell:~$ ls
Addadshashanammu.zip  README.txt
CharlyRod-picoctf@webshell:~$ unzip  
.ssh/                 Addadshashanammu.zip  
CharlyRod-picoctf@webshell:~$ unzip 
.ssh/                 Addadshashanammu.zip  
CharlyRod-picoctf@webshell:~$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
 extracting: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet.c  
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
CharlyRod-picoctf@webshell:~$ ls
Addadshashanammu  Addadshashanammu.zip  README.txt
CharlyRod-picoctf@webshell:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
CharlyRod-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet  fang-of-haynekhtnamet.c
CharlyRod-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
CharlyRod-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ 
```
picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
### Notas adicionales

### Referencias