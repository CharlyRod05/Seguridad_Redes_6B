### Picker IV
### Descripcion
Can you figure out how this program works to get the flag?

Connect to the program with netcat:

`$ nc saturn.picoctf.net 59513`

The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV).
### Solucion
```
┌──(kali㉿kali)-[~/reversing2/4picker]
└─$ nm ./picker-IV | grep " T "                    
00000000004011c0 T _dl_relocate_static_pie
0000000000401448 T _fini
0000000000401000 T _init
0000000000401440 T __libc_csu_fini
00000000004013d0 T __libc_csu_init
0000000000401334 T main
0000000000401276 T print_segf_message
0000000000401190 T _start
000000000040129e T win
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/reversing2/4picker]
└─$ nc saturn.picoctf.net 59513
Enter the address in hex to jump to, excluding '0x': 000000000040129e
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_01672a61}

```

picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_01672a61}
### Notas adicionales

### Referencias