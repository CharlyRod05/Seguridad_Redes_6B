### Secret of the Polyglot
### Descripcion
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/9/flag2of2-final.pdf).
### Solucion
el archivo es un .pdf pero al utilizar file nos dice que es un png, lo abrimos primero como pdf y nos muestra la parte final de la bandera, despues lo abrimos como png y nos muestra el inicio

```
┌──(kali㉿kali)-[~/forensic/SecretPolyglot]
└─$ open flag2of2-final.pdf 

┌──(kali㉿kali)-[~/forensic/SecretPolyglot]
└─$ file flag2of2-final.pdf 
flag2of2-final.pdf: PNG image data, 50 x 50, 8-bit/color RGBA, non-interlaced

┌──(kali㉿kali)-[~/forensic/SecretPolyglot]
└─$ mv flag2of2-final.pdf flag2of2-final.png 

┌──(kali㉿kali)-[~/forensic/SecretPolyglot]
└─$ open flag2of2-final.png 

```
picoCTF{f1u3n7_1n_pn9_&_pdf_7f9bccd1}
### Notas adicionales

### Referencias