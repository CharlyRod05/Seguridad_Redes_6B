### hideme
### Descripcion
Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/257/flag.png).
### Solucion
Al realizar un pngcheck sobre el archivo este menciona que hay datos despues del chunk IEND, esto indica que hay informacion oculta en esos bytes, luego analizando con hexeditor encontre una cadena ascii "secret/", esto parece indicar que hay una especie de estructura, es asi como probando con un unzip me mostro que se podia extraer la carpeta secret/ y dentro se encontraba una segunda imagen con la bandera.

```
┌──(kali㉿kali)-[~/forensic/hideme]
└─$ pngcheck -v flag.png 
File: flag.png (43020 bytes)
  chunk IHDR at offset 0x0000c, length 13
    512 x 504 image, 32-bit RGB+alpha, non-interlaced
  chunk IDAT at offset 0x00025, length 8192
    zlib: deflated, 32K window, fast compression
  chunk IDAT at offset 0x02031, length 8192
  chunk IDAT at offset 0x0403d, length 8192
  chunk IDAT at offset 0x06049, length 8192
  chunk IDAT at offset 0x08055, length 6866
  chunk IEND at offset 0x09b33, length 0
  additional data after IEND chunk
ERRORS DETECTED in flag.png


┌──(kali㉿kali)-[~/forensic/hideme]
└─$ unzip flag.png 
Archive:  flag.png
warning [flag.png]:  39739 extra bytes at beginning or within zipfile
  (attempting to process anyway)
   creating: secret/
  inflating: secret/flag.png         


┌──(kali㉿kali)-[~/forensic/hideme]
└─$ ls
flag.png  secret

```
### Notas adicionales

### Referencias