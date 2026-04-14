### Easy1
### Descripcion
The one time pad can be cryptographically secure, but not when you know the key. Can you solve this?We've given you the encrypted flag, key, and a table to help UFJKXQZQUNB with the key of SOLVECRYPTO. Can you use this [table](https://challenge-files.picoctf.net/c_fickle_tempest/859ffc313a4d8b63149f144745043a7312fc4f993e405eeeb8ee5ae6ca8444a8/table.txt) to solve it?.
### Solucion
Usando cyberchef y la receta para decodificar vigenere obtenemos la bandera al colocar el texto encriptado y la clave
picoCTF{CRYPTOISFUN}
### Notas adicionales
**El cifrado Vigenère** es una sustitución **polialfabética** que aplica una secuencia de desplazamientos derivados de una **palabra clave** repetida. A diferencia del [César](https://letscipher.com/es/cifrados/cesar), cada letra del mensaje se cifra con un alfabeto distinto, lo que frustra el análisis de frecuencia simple.

Se apoya de una tabla con el alfabeto desplazado 1 posicion por cada fila y utilizando la clave se obtiene un texto codificado.


### Referencias
[Vigenère Decode - CyberChef](https://cyberchef.org/#recipe=Vigen%C3%A8re_Decode\('SOLVECRYPTO'\)&input=VUZKS1hRWlFVTkIg)