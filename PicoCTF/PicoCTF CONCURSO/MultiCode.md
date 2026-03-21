### MultiCode
### Descripcion
We intercepted a suspiciously encoded message, but it’s clearly hiding a flag. No encryption, just multiple layers of obfuscation. Can you peel back the layers and reveal the truth?Download the [message](https://challenge-files.picoctf.net/c_plain_mesa/8599b14c39d96dfed1a6c99aea6038e475aa23326763ee7f9547796a952219b4/message.txt).

NjM3NjcwNjI1MDQ3NTMyNTM3NDI2MTcyNjY2NzcyNzE1ZjcyNjE3MDMwNzE3NjYxNzQ1ZjczNzM2ZjM2NzA2ZTZlMzIyNTM3NDQ=
### Solución
utilizando cyberchef logramos quitar la ofuscación al mensaje decodificando desde hexa, base 64, url y rot13, se adjunta el cyberchef en las referencias
### Notas adicionales

### Referencias
[From Base64, From Hex, URL Decode, ROT13 - CyberChef](https://cyberchef.org/#recipe=From_Base64\('A-Za-z0-9%2B/%3D',true,false\)From_Hex\('Auto'\)URL_Decode\(\)ROT13\(true,true,false,13\)&input=TmpNM05qY3dOakkxTURRM05UTXlOVE0zTkRJMk1UY3lOalkyTnpjeU56RTFaamN5TmpFM01ETXdOekUzTmpZeE56UTFaamN6TnpNMlpqTTJOekEyWlRabE16SXlOVE0zTkRRPQ)