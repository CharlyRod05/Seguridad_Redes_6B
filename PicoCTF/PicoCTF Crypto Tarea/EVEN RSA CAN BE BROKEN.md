### EVEN RSA CAN BE BROKEN???

### Descripcion
This service provides you an encrypted flag. Can you decrypt it with just N & e?Connect to the program with netcat:

`$ nc verbal-sleep.picoctf.net 49796`The program's source code can be downloaded [here](https://challenge-files.picoctf.net/c_verbal_sleep/968ace6e870166b1d910d69fe174b6ce7de6ece89448ab5d693a19c052b3d2b4/encrypt.py).
### Solucion
Codigo base
```
from sys import exit
from Crypto.Util.number import bytes_to_long, inverse
from setup import get_primes

e = 65537

def gen_key(k):
    """
    Generates RSA key with k bits
    """
    p,q = get_primes(k//2)
    N = p*q
    d = inverse(e, (p-1)*(q-1))

    return ((N,e), d)

def encrypt(pubkey, m):
    N,e = pubkey
    return pow(bytes_to_long(m.encode('utf-8')), e, N)

def main(flag):
    pubkey, _privkey = gen_key(1024)
    encrypted = encrypt(pubkey, flag) 
    return (pubkey[0], encrypted)

if __name__ == "__main__":
    flag = open('flag.txt', 'r').read()
    flag = flag.strip()
    N, cypher  = main(flag)
    print("N:", N)
    print("e:", e)
    print("cyphertext:", cypher)
    exit()
```
los n que nos retorna el programa son todos par, lo que indica que uno de los factores es 2 y con el podemos calcular el segundo

N = 15550395955046384591449010676925141880599227831917738782030677986535431154884933734853907590782788264307880327998586971258418659479761299676050787838243362
e = 65537
c = 12447401802971648307474078839352366811085325830706405208595566462783547236798040703716085256823413442332113148474433553895305916019071905763018524112201985

p = 2
q = 7775197977523192295724505338462570940299613915958869391015338993267715577442466867426953795391394132153940163999293485629209329739880649838025393919121681
d = 7775197977523192295724505338462570940299613915958869391015338993267715577442466867426953795391394132153940163999293485629209329739880649838025393919121681

picoCTF{tw0_1$_pr!m37dbe6984}

use esta pagina para desencriptar [RSA Cipher Calculator - Online Decoder, Encoder, Translator](https://www.dcode.fr/rsa-cipher)
### Notas adicionales

### Referencias