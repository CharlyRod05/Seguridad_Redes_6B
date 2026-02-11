### First Find
### Descripcion
Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/500/files.zip)
### Solucion
```
CharlyRod-picoctf@webshell:~$ unzip files.zip 
Archive:  files.zip
   creating: files/
   creating: files/satisfactory_books/
   creating: files/satisfactory_books/more_books/
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8  
  inflating: files/satisfactory_books/23765.txt.utf-8  
  inflating: files/satisfactory_books/16021.txt.utf-8  
  inflating: files/13771.txt.utf-8   
   creating: files/adequate_books/
   creating: files/adequate_books/more_books/
   creating: files/adequate_books/more_books/.secret/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt  
  inflating: files/adequate_books/more_books/1023.txt.utf-8  
  inflating: files/adequate_books/46804-0.txt  
  inflating: files/adequate_books/44578.txt.utf-8  
   creating: files/acceptable_books/
   creating: files/acceptable_books/more_books/
  inflating: files/acceptable_books/more_books/40723.txt.utf-8  
  inflating: files/acceptable_books/17880.txt.utf-8  
  inflating: files/acceptable_books/17879.txt.utf-8  
  inflating: files/14789.txt.utf-8   
CharlyRod-picoctf@webshell:~$ grep pico -r files
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt:picoCTF{f1nd_15_f457_ab443fd1}
files/14789.txt.utf-8:brassa un picotin d'orge_. Comme depuis une demi-heure environ c'était
CharlyRod-picoctf@webshell:~$ 
```
picoCTF{f1nd_15_f457_ab443fd1}

### Solucion 2 con find
```
CharlyRod-picoctf@webshell:~$ find -name uber*
./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
CharlyRod-picoctf@webshell:~$ cat ./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
picoCTF{f1nd_15_f457_ab443fd1}
```
picoCTF{f1nd_15_f457_ab443fd1}
### Notas adicionales
Grep -r es todopoderoso

Se debia utilizar find para encontrar el archivo uber_secret y simplemente usar cat pero grep puede con todo.
### Referencias
