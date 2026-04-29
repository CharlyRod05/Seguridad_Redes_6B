### hashcrack

### Descripcion
A company stored a secret message on a server which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server?Access the server using `nc verbal-sleep.picoctf.net 57371`
### Solucion
hash: 482c811da5d5b4bc6d497ffa98491e38
con esto podemos ver que el algoritmo es md4 o md5, lo pasamos por un decriptador de hashes que prueba contraseñas inseguras y tenemos:
 
password123

el programa nos regresa otro hash ahora mas largo que probablemente es SHA1
Flag is yet to be revealed!! Crack this hash: b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3

letmein

Nos arroja un ultimo hash y al decriptarlo obtenemos que estaba en SHA256

916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745
qwerty098
picoCTF{UseStr0nG_h@shEs_&PaSswDs!_eb2f8459}
### Notas adicionales

### Referencias
[Decrypt MD5, SHA1, MySQL, NTLM, SHA256, MD5 Email, SHA256 Email, SHA512, Wordpress, Bcrypt hashes for free online](https://hashes.com/en/decrypt/hash)