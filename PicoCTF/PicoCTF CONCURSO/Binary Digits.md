# Reto
# Descripcion
This file doesn't look like much... just a bunch of 1s and 0s. But maybe it's not just random noise. Can you recover anything meaningful from this?Download the file [here](https://challenge-files.picoctf.net/c_plain_mesa/f6919e2dcefe1ca2658b9f8d0c26d517822769325bc7fed5b27e3e68563dcc77/digits.bin).
# Solucion

```
vladi@911:~/Desktop/retos/reto$ python3 -c "import sys; data = open('digits.bin').read().strip(); sys.stdout.buffer.write(bytes([int(data[i:i+8], 2) for i in range(0, len(data), 8)]))" > flag.png
vladi@911:~/Desktop/retos/reto$ file flag.png 
flag.png: JPEG image data, JFIF standard 1.01, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 800x500, components 3

```
### Flag: picoCTF{h1dd3n_1n_th3_b1n4ry_a59b2b0a}
# Notas
Al imprimir con cat mostro puros 0 y 1  supuse que la bandera viene encriptada en el binario, para extraer la bandera utilice un comando en python para combertir el binario a ascii, pero mostro una cantidad de simbolos sin sentido probablemente no es texto y es una imagen, en lugar de imprimir en terminal lo puse en un archivo .png y al abrirlo venia la bandera en la imagen.

# Referencias
