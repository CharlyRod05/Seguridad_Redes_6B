# Reto
# Descripcion
Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz).
# Solucion

```
vladi@911:~/Desktop/retos/reto$ gzip -d fixme1.tar.gz
vladi@911:~/Desktop/retos/reto$ ls
fixme1.tar
vladi@911:~/Desktop/retos/reto$ tar xpf fixme1.tar
vladi@911:~/Desktop/retos/reto$ ls
fixme1  fixme1.tar
vladi@911:~/Desktop/retos/reto$ ls fixme1
Cargo.lock  Cargo.toml  src
vladi@911:~/Desktop/retos/reto$ cd fixme1/src/
vladi@911:~/Desktop/retos/reto/fixme1/src$ cargo run main
    Updating crates.io index
  Downloaded crossbeam-deque v0.8.5
  Downloaded xor_cryptor v1.2.3
  Downloaded rayon-core v1.12.1
  Downloaded either v1.13.0
  Downloaded crossbeam-utils v0.8.20
  Downloaded crossbeam-epoch v0.9.18
  Downloaded rayon v1.10.0
  Downloaded 7 crates (379.2KiB) in 0.50s
   Compiling crossbeam-utils v0.8.20
   Compiling rayon-core v1.12.1
   Compiling either v1.13.0
   Compiling crossbeam-epoch v0.9.18
   Compiling crossbeam-deque v0.8.5
   Compiling rayon v1.10.0
   Compiling xor_cryptor v1.2.3
   Compiling rust_proj v0.1.0 (/home/vladi/Desktop/retos/reto/fixme1)
error: expected `;`, found keyword `let`
 --> src/main.rs:5:37
  |
5 |     let key = String::from("CSUCKS") // How do we end statements in Rust?
  |                                     ^ help: add `;` here
...
8 |     let hex_values = ["41", "30", "20", "63", "4a", "45", "54", "76", "01", "1c", "7e", "59", "63", "e1", "61", "25", "7f", "5a", "60", "50", "11", "38", "1f", "3a", "60", "e9", "62", "20", "0c", "e6",...
  |     --- unexpected token

error: argument never used
  --> src/main.rs:26:9
   |
25 |         ":?", // How do we print out a variable in the println function? 
   |         ---- formatting specifier missing
26 |         String::from_utf8_lossy(&decrypted_buffer)
   |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ argument never used
   |
help: format specifiers use curly braces, consider adding a format specifier
   |
25 |         ":?{}", // How do we print out a variable in the println function? 
   |            ++

error[E0425]: cannot find value `ret` in this scope
  --> src/main.rs:18:9
   |
18 |         ret; // How do we return in rust?
   |         ^^^
   |
help: a local variable with a similar name exists
   |
18 -         ret; // How do we return in rust?
18 +         res; // How do we return in rust?
   |

For more information about this error, try `rustc --explain E0425`.
error: could not compile `rust_proj` (bin "rust_proj") due to 3 previous errors
vladi@911:~/Desktop/retos/reto/fixme1/src$ nano main.rs
vladi@911:~/Desktop/retos/reto/fixme1/src$ cargo run main
   Compiling rust_proj v0.1.0 (/home/vladi/Desktop/retos/reto/fixme1)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.09s
     Running `/home/vladi/Desktop/retos/reto/fixme1/target/debug/rust_proj main`
picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}
```
### Flag: picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}

# Notas
Descomprimi el archivo con gzip y tar, adento venia un main.rs, lo ejecute con el comando cargo run. El compilador me tiro 3 errores, un ;, escribir return y la funcion print le faltaba {}. Despues de arreglarlo y volverlo a compilar me dio la bandera. 
# Referencias
