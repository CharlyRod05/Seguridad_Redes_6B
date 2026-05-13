## asm3
### Descripcion
What does asm3(0xdb5bc7fb,0xd5781141,0xc7d66f97) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/64f65c2cd120e568d93fc10d4cce2d3f1c163fa67f980d36736f6abd8b9481a5/test.S)
### Solucion

p1 = 0xdb5bc7fb
p2 = 0xd5781141
p3 = 0xc7d66f97

- `[ebp+0xb]` = 11 → byte 4 de p1 = **0xdb**
- `[ebp+0xd]` = 13 → byte 2 de p2 = **0x11** 
    
- `[ebp+0xf]` = 15 → byte 4 (MSB) de p2 = **0xd5**
    
- `[ebp+0x12]` = 18 → palabra (2 bytes) en p3: bytes en 18=0xd6 (LSB), 19=0xc7 (MSB) → valor **0xc7d6**


```
xor eax, eax                ; eax = 0x00000000
mov ah, BYTE PTR [ebp+0xb]  ; ah = 0xdb → eax = 0x0000db00
shl ax, 0x10                ; ax = 0xdb00 << 16 = 0x0000 → eax = 0x00000000
                            ; (se pierde todo, el 0xdb desaparece)
sub al, BYTE PTR [ebp+0xd]  ; al = 0x00 - 0x11 = 0xef → eax = 0x000000ef
add ah, BYTE PTR [ebp+0xf]  ; ah = 0x00 + 0xd5 = 0xd5 → eax = 0x0000d5ef
xor ax, WORD PTR [ebp+0x12] ; ax = 0xd5ef ^ 0xc7d6 = 0x1239 → eax = 0x00001239
```
Los 0s no se escriben y nos queda
0x1239
### Notas adicionales

### Referencias