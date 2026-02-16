### runme.py

### Descripcion
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
### Solucion
```
CharlyRod-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2026-02-16 13:51:27--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py                     100%[=============================================>]     270  --.-KB/s    in 0s      

2026-02-16 13:51:27 (182 MB/s) - 'runme.py' saved [270/270]

CharlyRod-picoctf@webshell:~$ ls
README.txt  runme.py
CharlyRod-picoctf@webshell:~$ python runme.py 
picoCTF{run_s4n1ty_run}
CharlyRod-picoctf@webshell:~$ 
```
### Notas adicionales

### Referencias
