# Reto
# Descripcion
Python scripts are invoked kind of like programs in the Terminal...Can you run [ende.py](https://challenge-files.picoctf.net/c_wily_courier/a4c97b512a4e6de24045ab3e8294651bcfc241ce571daa8afdad3c35885ffa60/ende.py) using [password.txt](https://challenge-files.picoctf.net/c_wily_courier/a4c97b512a4e6de24045ab3e8294651bcfc241ce571daa8afdad3c35885ffa60/password.txt) to get [flag.txt.en](https://challenge-files.picoctf.net/c_wily_courier/a4c97b512a4e6de24045ab3e8294651bcfc241ce571daa8afdad3c35885ffa60/flag.txt.en)?
# Solucion

```
vladi@911:~/Desktop/retos/reto$ ls
ende.py  flag.txt.en  password.txt
vladi@911:~/Desktop/retos/reto$ python3 ende.py 
Usage: ende.py (-e/-d) [file]
vladi@911:~/Desktop/retos/reto$ cat password.txt 
720b6ad346f84cd483c60c7464dd95d4
vladi@911:~/Desktop/retos/reto$ python3 ende.py -d flag.txt.en 
Please enter the password:720b6ad346f84cd483c60c7464dd95d4
picoCTF{4p0110_1n_7h3_h0us3_9c5f9bcf}

```
### Flag: picoCTF{4p0110_1n_7h3_h0us3_9c5f9bcf}
# Notas
Descargue los archivos, vi que habia un .py,dun archivo cifrado y un password, corri el py y me mencionaba que agregara un argumento para encriptar o desencriptar junto al nombre de un archivo, imprimi el password, llame al .py y agregue como argumento desencriptar el archivo cifrado. Solicito el password, se la agregue y me dio la bandera.
# Referencias
