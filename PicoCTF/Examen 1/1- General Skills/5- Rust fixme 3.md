# Reto
# Descripcion
Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/dcdaf491b35c1d0f5075e9583edbbb7aaea1dffb6ad32bc000e4d87b5200ff7b/fixme3.tar.gz).
# Solucion

```
vladi@911:~/Desktop/retos/reto$ gzip -d fixme3.tar.gz 
vladi@911:~/Desktop/retos/reto$ tar xpf fixme3.tar 
vladi@911:~/Desktop/retos/reto$ cd fixme3/src/
vladi@911:~/Desktop/retos/reto/fixme3/src$ ls
main.rs
vladi@911:~/Desktop/retos/reto/fixme3/src$ cargo run main
   Compiling crossbeam-utils v0.8.20
   Compiling rayon-core v1.12.1
   Compiling either v1.13.0
   Compiling crossbeam-epoch v0.9.18
   Compiling crossbeam-deque v0.8.5
   Compiling rayon v1.10.0
   Compiling xor_cryptor v1.2.3
   Compiling rust_proj v0.1.0 (/home/vladi/Desktop/retos/reto/fixme3)
error[E0133]: call to unsafe function `std::slice::from_raw_parts` is unsafe and requires unsafe function or block
  --> src/main.rs:31:31
   |
31 |         let decrypted_slice = std::slice::from_raw_parts(decrypted_ptr, decrypted_len);
   |                               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ call to unsafe function
   |
   = note: consult the function's documentation for information on how to avoid undefined behavior

For more information about this error, try `rustc --explain E0133`.
error: could not compile `rust_proj` (bin "rust_proj") due to 1 previous error

vladi@911:~/Desktop/retos/reto/fixme3/src$ nano main.rs 
vladi@911:~/Desktop/retos/reto/fixme3/src$ cargo run main
   Compiling rust_proj v0.1.0 (/home/vladi/Desktop/retos/reto/fixme3)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.10s
     Running `/home/vladi/Desktop/retos/reto/fixme3/target/debug/rust_proj main`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: picoCTF{n0w_y0uv3_f1x3d_1h3m_411}

```
### Flag: picoCTF{n0w_y0uv3_f1x3d_1h3m_411}
# Notas
Descomprimi el archivo con gzip y tar, adento venia un main.rs, lo ejecute con el comando cargo run. El compilador tiro un error raro, revisando el codigo miraba el codigo bien hasta que vi que hay un bloque llamado usafe comentado, lo corregi y al compilar me dio la bandera.
# Referencias
