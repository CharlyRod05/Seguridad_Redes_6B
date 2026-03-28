# Reto
# Descripcion
Connect to this PostgreSQL server and find the flag!

Additional details will be available after launching your challenge instance.
# Solucion

```
vladi@911:~$ psql -h saturn.picoctf.net -p 49209 -U postgres pico
Password for user postgres: 
psql (18.3 (Debian 18.3-1+b1), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=# -help
pico-# --help
pico-# help
Use \? for help or press control-C to clear the input buffer.
pico-# \?
pico-# \d
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico-# select * from flags;
ERROR:  syntax error at or near "-"
LINE 1: -help
        ^
pico=# Select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

```
### Flag: picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
# Notas
Al abrir conectarme intente usar help para ver los comandos del postgres, al parecer puedo ver las tablas escribiendo \d, hay una tabla llamada flags, al ver  los registros de la tabla habia uno con la bandera.
# Referencias
