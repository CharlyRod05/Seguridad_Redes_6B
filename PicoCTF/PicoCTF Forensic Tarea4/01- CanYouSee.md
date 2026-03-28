### CanYouSee
### Descripcion
How about some hide and seek?Download this file [here](https://artifacts.picoctf.net/c_titan/5/unknown.zip).
### Solucion
Busque los metadatos del archivo y encontre que el url se veia extraño y estaba codificado en base64, con cyberchef lo decodifique y obtuve la bandera
```
┌──(kali㉿kali)-[~/forensic/canyuSee]
└─$ exiftool ukn_reality.jpg 
ExifTool Version Number         : 13.36
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:02:15 17:40:17-05:00
File Access Date/Time           : 2026:03:28 11:32:10-04:00
File Inode Change Date/Time     : 2026:03:28 11:29:43-04:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fNGRhYmRkY2J9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4

```
attribution URL decodificado:

picoCTF{ME74D47A_HIDD3N_4dabddcb}
### Notas adicionales

### Referencias
[From Base64 - CyberChef](https://cyberchef.org/#recipe=From_Base64\('A-Za-z0-9%2B/%3D',true,false\)&input=Y0dsamIwTlVSbnROUlRjMFJEUTNRVjlJU1VSRU0wNWZOR1JoWW1Sa1kySjlDZz09DQo)