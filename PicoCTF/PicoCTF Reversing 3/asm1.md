## asm1
### Descripcion
What does asm1(0x2ff) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/936da3d33f13bd9c9153ad7e9974c2fe51c00da410fa43567caa790ed56f9346/test.S)
### Solucion


El codigo traducido hace esto con el parametro dado

|Paso|Lo que hace la función|¿Qué pasa con 767?|
|---|---|---|
|Compara si **> 0x753 (1875)**|767 > 1875?|**No** → va a la rama `<= 1875`|
|Compara si **== 0x5af (1455)**|767 == 1455?|**No** → va al `jne`|
|Carga el valor original a `eax`|`mov eax, 767`|✅|
|Resta 7|`sub eax, 7` → 767 - 7|**760**|
|Salta al final y retorna|`ret`|Devuelve **760**|
Resultado hexa:
0x2f8
### Notas adicionales

### Referencias