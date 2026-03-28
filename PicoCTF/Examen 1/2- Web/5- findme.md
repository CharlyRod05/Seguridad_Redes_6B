# Reto
# Descripcion
Help us test the form by submiting the username as `test` and password as `test!`The website running [here](http://saturn.picoctf.net:54825/).
# Solucion

```
1- http://saturn.picoctf.net:54825/
2- http://saturn.picoctf.net:54825/next-page/id=bF90aGVfd2F5X2JlNzE2ZDhlfQ==
3- http://saturn.picoctf.net:54825/next-page/id=cGljb0NURntwcm94aWVzX2Fs
4- http://saturn.picoctf.net:54825/home
```
[segunda parte bandera](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YkY5MGFHVmZkMkY1WDJKbE56RTJaRGhsZlE9PQ&oeol=NEL)
[primera parte bandera](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnR3Y205NGFXVnpYMkZz&oeol=NEL)
### Flag: picoCTF{proxies_all_the_way_be716d8e}
# Notas
Al loguearme con las credenciales que me recomienda el reto me di cuenta que la pagina pasa por unos directorios antes de entrar al home, los decodifique con cyberchef y me dio la bandera en 2 partes.
# Referencias
