### Operation Orchid
### Descripcion
Download this disk image and find the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/214/disk.flag.img.gz)
### Solucion

Se busca el archivo de flag en el disco y se saca, viendo el bash history encontramos el comando usado para encriptarla y lo reproducimos en nuestra maquina a la inversa
```
┌──(kali㉿kali)-[~/forensic/operationOrchid]
└─$ icat -o 0000411648 disk.flag.img 1782 > flag.txt.enc
                                                                             
┌──(kali㉿kali)-[~/forensic/operationOrchid]
└─$ cat flag.txt.enc 
Salted__S�+%���+�O��k�ђ(A����c��
                                @]ԣ
L�ޢȤ7� ���؎$�'%                                                                             
┌──(kali㉿kali)-[~/forensic/operationOrchid]
└─$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567

*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
4067C54E137F0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107:
                                                                             
┌──(kali㉿kali)-[~/forensic/operationOrchid]
└─$ cat flag.txt    
picoCTF{h4un71ng_p457_1d02081e}  
```

picoCTF{h4un71ng_p457_1d02081e}
### Notas adicionales

### Referencias