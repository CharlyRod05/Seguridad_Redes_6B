### fixme2.py
### Descripcion
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/4/fixme2.py)
### Solucion
```
CharlyRod-picoctf@webshell:~$ python fixme2.py 
  File "/home/CharlyRod-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
CharlyRod-picoctf@webshell:~$ nano fixme2.py 
CharlyRod-picoctf@webshell:~$ nano fixme2.py 
CharlyRod-picoctf@webshell:~$ python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
CharlyRod-picoctf@webshell:~$ 
```
### Notas adicionales
solo se coloca un == en lugar del =
### Referencias
