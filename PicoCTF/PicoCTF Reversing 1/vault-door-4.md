### vault-door-4
### Descripcion
This vault uses ASCII encoding for the password.The source code for this vault is here: [VaultDoor4.java](https://challenge-files.picoctf.net/c_fickle_tempest/5a242afc9022df976b1c18fe9364788579431217536fca41006714b29d8931e1/VaultDoor4.java)
### Solucion
codigo modificado:
```
byte[] myBytes = {
            106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0142, 0131, 0164, 063 , 0163, 0137, 040 , 063 ,
            '0' , 'd' , 'c' , '8' , '5' , 'b' , 'e' , 'd' ,
        };
        String flag = new String(myBytes); //añadido
        System.out.println(flag); //añadido

```
solo conviertes los bytes a string y los imprimes para ver la contraseña

```
Enter vault password: PicoCTF{}
jU5t_4_bUnCh_0f_bYt3s_ 30dc85bed
```

PicoCTF{jU5t_4_bUnCh_0f_bYt3s_ 30dc85bed}
### Notas adicionales

### Referencias
