### Pixelated
### Descripcion
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://challenge-files.picoctf.net/c_wily_courier/2180f74b7f56abc330252d0146f6a044f8e35027142e5cb16c9160c37a0c630f/scrambled1.png) [scrambled2.png](https://challenge-files.picoctf.net/c_wily_courier/2180f74b7f56abc330252d0146f6a044f8e35027142e5cb16c9160c37a0c630f/scrambled2.png)
### Solucion
Las imagenes se convierten a matriz y se suman, la imagen resultante si es legible y contiene la bandera

```
from PIL import Image
import numpy as np

imagen1 = np.asarray( Image.open('scrambled1.png') )
imagen2 = np.asarray( Image.open('scrambled2.png') )

data = imagen1 + imagen2

nueva = Image.fromarray(data)
nueva.save("out.png", "PNG")
```

picoCTF{8cdf93c3}
### Notas adicionales

### Referencias
