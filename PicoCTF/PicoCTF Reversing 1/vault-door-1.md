### vault-door-1
### Descripcion
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://challenge-files.picoctf.net/c_fickle_tempest/eb2eaca69cb975c96a289b4db182ed439cf7f6bc542b135b8a9a1e9834c068c1/VaultDoor1.java)
### Solucion
En el codigo extraje la parte del password a un archivo flag y agregue 0 a los numeros con solo 1 digito para que sort funcione, luego con ese archivo use el siguiente comando para extraer la 3er columna y que elimine las comillas y saltos de linea
```
cat flag | sort | awk '{print($3)}' | tr -d "'" | tr -d "\n"
d35cr4mbl3_tH3_cH4r4cT3r5_29e8d8
```

PicoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_29e8d8} 
### Notas adicionales

### Referencias
