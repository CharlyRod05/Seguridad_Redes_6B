### credstuff

### Descripcion
We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it?Download the leak [here](https://artifacts.picoctf.net/c/151/leak.tar).The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.
### Solucion
con un comando sencillo y directo en terminal obtuve la linea donde aparecia cultiris e imprimi la linea correspondiente del otro archivo

```
CharlyRod-picoctf@webshell:~/leak$ linea=$(grep -n "cultiris" usernames.txt | cut -d: -f1) && sed -n " ${linea}p" passwords.txt 
cvpbPGS{P7e1S_54I35_71Z3}
```
ya solo es un rot13 con cyberchef y tenemos
picoCTF{C7r1F_54V35_71M3}
### Notas adicionales

### Referencias
[ROT13 - CyberChef](https://cyberchef.org/#recipe=ROT13\(true,true,false,13\)&input=Y3ZwYlBHU3tQN2UxU181NEkzNV83MVozfQ)