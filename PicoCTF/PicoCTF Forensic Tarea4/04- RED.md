### RED
### Descripcion
RED, RED, RED, REDDownload the image: [red.png](https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png)
### Solucion
Al mirar los metadatos me encontre un poema sospechoso, si revisas las mayusculas del poema forman "check lsb" y despues utilizando zsteg encontre en el lsb un texto codificado en base 64, lo decodifique y obtuve la bandera

```
┌──(kali㉿kali)-[~/forensic/RED]
└─$ exiftool red.png
ExifTool Version Number         : 13.36
File Name                       : red.png
Directory                       : .
File Size                       : 796 bytes
File Modification Date/Time     : 2025:03:05 22:34:15-05:00
File Access Date/Time           : 2026:03:28 12:56:29-04:00
File Inode Change Date/Time     : 2026:03:28 12:56:24-04:00
File Permissions                : -rw-rw-r--
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 128
Image Height                    : 128
Bit Depth                       : 8
Color Type                      : RGB with Alpha
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Poem                            : Crimson heart, vibrant and bold,.Hearts flutter at your sight..Evenings glow softly red,.Cherries burst with sweet life..Kisses linger with your warmth..Love deep as merlot..Scarlet leaves falling softly,.Bold in every stroke.
Image Size                      : 128x128
Megapixels                      : 0.016
                                                                     
┌──(kali㉿kali)-[~/forensic/RED]
└─$ zsteg red.png 
meta Poem           .. text: "Crimson heart, vibrant and bold,\nHearts flutter at your sight.\nEvenings glow softly red,\nCherries burst with sweet life.\nKisses linger with your warmth.\nLove deep as merlot.\nScarlet leaves falling softly,\nBold in every stroke."                                                                                                                                                                                                                
chunk:0:IHDR        .. file: Adobe Photoshop Color swatch, version 0, 128 colors; 1st RGB space (0), w 0x80, x 0x806, y 0, z 0; 2nd HSB space (1), w 0x100, x 0, y 0xff01, z 0xff
b1,rgba,lsb,xy      .. text: "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ=="
```
cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==
decoded:
picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}

### Notas adicionales

### Referencias
[From Base64 - CyberChef](https://cyberchef.org/#recipe=From_Base64\('A-Za-z0-9%2B/%3D',true,false\)&input=Y0dsamIwTlVSbnR5TTJSZk1YTmZkR2d6WDNWc2RERnROSFF6WDJOMWNqTmZaakJ5WHpVMFpHNHpOVFZmZlE9PWNHbGpiME5VUm50eU0yUmZNWE5mZEdnelgzVnNkREZ0TkhRelgyTjFjak5mWmpCeVh6VTBaRzR6TlRWZmZRPT1jR2xqYjBOVVJudHlNMlJmTVhOZmRHZ3pYM1ZzZERGdE5IUXpYMk4xY2pOZlpqQnlYelUwWkc0ek5UVmZmUT09Y0dsamIwTlVSbnR5TTJSZk1YTmZkR2d6WDNWc2RERnROSFF6WDJOMWNqTmZaakJ5WHpVMFpHNHpOVFZmZlE9PQ)