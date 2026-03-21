
**Descripción** 
After logging in, you will find multiple file parts in your home directory. These parts need to be combined and extracted to reveal the flag.
Additional details will be available after launching your challenge instance.

**Solución**  
- Conectarse con: ssh -p 49897 ctf-player@dolphin-cove.picoctf.net
- Contraseña: 84b12bae
- Listar archivos: ls -la
- Combinar los archivos en un solo archivo: cat files.tar.gz.part* > files.tar.gz
- Extraer el contwnido: unzip combined.tar
- Hacer un cat a las instrucciones para ver la contraseña
- Poner la contraseña :supersecret
- Bandera: picoCTF{z1p_and_spl1t_f1l3s_4r3_fun_78b76e61}