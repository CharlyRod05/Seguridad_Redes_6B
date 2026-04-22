### HideToSee
### Descripcion
How about some hide and seek heh? Look at this image [here](https://artifacts.picoctf.net/c/237/atbash.jpg).
### Solucion
con steghide extraemos
```
┌──(kali㉿kali)-[~/cry]
└─$ steghide --extract -sf atbash.jpg
Enter passphrase: 
wrote extracted data to "encrypted.txt".
                                                                             
┌──(kali㉿kali)-[~/cry]
└─$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_05y2z65z}

```
con cyberchef desencriptamos
[Atbash Cipher - CyberChef](https://cyberchef.org/#recipe=Atbash_Cipher\(\))
picoCTF{atbash_crack_05b2a65a}
### Notas adicionales

### Referencias
