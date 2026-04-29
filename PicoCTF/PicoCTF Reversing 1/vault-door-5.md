### vault-door-5
### Descripcion
In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding!The source code for this vault is here: [VaultDoor5.java](https://challenge-files.picoctf.net/c_fickle_tempest/bd4f8f70a70dacc0e57dfc24ff34f5297a3db3c9c4366fd8df02f6bf47c794c8/VaultDoor5.java)
### Solucion
En el codigo fuente aparece esta password
JTYzJTMwJTZlJTc2JTMzJTcyJTc0JTMxJTZlJTY3JTVmJTY2JTcyJTMwJTZkJTVmJTYyJTYxJTM1JTY1JTVmJTM2JTM0JTVmJTYyJTY1JTM5JTY2JTMxJTMwJTYxJTM0

solo le quitamos el base 64 y decodificamos el url y obtenemos
c0nv3rt1ng_fr0m_ba5e_64_be9f10a4

la bandera es:
PicoCTF{c0nv3rt1ng_fr0m_ba5e_64_be9f10a4}
### Notas adicionales

### Referencias