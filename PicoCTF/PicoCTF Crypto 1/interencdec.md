### interencdec
### Descripcion
Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/2/enc_flag).
### Solucion
El archivo contiene la bandera oculta bajo varias capas de encriptacion, primero decodificas base 64 eliminas caracteres extra, lo decodificas con otro base 64 y por ultimo rotas las letras 19 posiciones
picoCTF{caesar_d3cr9pt3d_78250afc}
### Notas adicionales

### Referencias
[From Base64, Tail, From Base64, ROT13 - CyberChef](https://cyberchef.org/#recipe=From_Base64\('A-Za-z0-9%2B/%3D',true,false\)Tail\('Nothing%20\(separate%20chars\)',50\)From_Base64\('A-Za-z0-9%2B/%3D',true,false\)ROT13\(true,true,false,19\)&input=WWlka00wSnhaR3R3UWxSWWRIRmhSM2cyWVVoc1ptRjZUbkZsVkd3eldWUk9jbGg2WXpSTmFsVjNZVWN4Y1daUlBUMG5DZz09)