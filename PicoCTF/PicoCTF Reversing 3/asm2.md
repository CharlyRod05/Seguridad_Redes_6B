## asm2
### Descripcion
What does asm2(0x8,0x2e) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/e52eb78a50fe37d5d90fa3200de17edb7b6e51a3e01c583cec0ed94d9e9bc306/test.S)
### Solucion
el codigo assembler lo podemos traducir a c++ y representaria esto
```c++
int asm2(int a, int b) {
    int local_a = a;
    int local_b = b;
    
    while (local_a <= 0xe6da) {  // 59098
        local_b = local_b + 1;
        local_a = local_a + 0xed;  // 237
    }
    
    return local_b;
}
```
con los parametros dados el resultado es 
0x128

da 250 vueltas en el bucle antes de superar el valor 0xe6da
por lo que 0x8 + 250 = 0x128
### Notas adicionales

### Referencias