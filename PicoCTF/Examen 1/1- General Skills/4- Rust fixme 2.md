# Reto
# Descripcion
The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz).
# Solucion

```
vladi@911:~/Desktop/retos/reto$ ls
fixme2.tar.gz
vladi@911:~/Desktop/retos/reto$ gzip -d fixme2.tar.gz 
vladi@911:~/Desktop/retos/reto$ ls
fixme2.tar
vladi@911:~/Desktop/retos/reto$ tar xpf fixme2.tar 
vladi@911:~/Desktop/retos/reto$ ls
fixme2  fixme2.tar
vladi@911:~/Desktop/retos/reto$ ls fixme2
Cargo.lock  Cargo.toml  src
vladi@911:~/Desktop/retos/reto$ cd fixme2/src/
vladi@911:~/Desktop/retos/reto/fixme2/src$ ls
main.rs
vladi@911:~/Desktop/retos/reto/fixme2/src$ cargo run main
   Compiling crossbeam-utils v0.8.20
   Compiling rayon-core v1.12.1
   Compiling either v1.13.0
   Compiling crossbeam-epoch v0.9.18
   Compiling crossbeam-deque v0.8.5
   Compiling rayon v1.10.0
   Compiling xor_cryptor v1.2.3
   Compiling rust_proj v0.1.0 (/home/vladi/Desktop/retos/reto/fixme2)
error[E0596]: cannot borrow `*borrowed_string` as mutable, as it is behind a `&` reference
 --> src/main.rs:9:5
  |
9 |     borrowed_string.push_str("PARTY FOUL! Here is your flag: ");
  |     ^^^^^^^^^^^^^^^ `borrowed_string` is a `&` reference, so it cannot be borrowed as mutable
  |
help: consider changing this to be a mutable reference
  |
3 | fn decrypt(encrypted_buffer:Vec<u8>, borrowed_string: &mut String){ // How do we pass values to a function that we want to change?
  |                                                        +++

error[E0596]: cannot borrow `*borrowed_string` as mutable, as it is behind a `&` reference
  --> src/main.rs:20:5
   |
20 |     borrowed_string.push_str(&String::from_utf8_lossy(&decrypted_buffer));
   |     ^^^^^^^^^^^^^^^ `borrowed_string` is a `&` reference, so it cannot be borrowed as mutable
   |
help: consider changing this to be a mutable reference
   |
 3 | fn decrypt(encrypted_buffer:Vec<u8>, borrowed_string: &mut String){ // How do we pass values to a function that we want to change?
   |                                                        +++

For more information about this error, try `rustc --explain E0596`.
error: could not compile `rust_proj` (bin "rust_proj") due to 2 previous errors
vladi@911:~/Desktop/retos/reto/fixme2/src$ nano main.rs 
vladi@911:~/Desktop/retos/reto/fixme2/src$ cargo run main
   Compiling rust_proj v0.1.0 (/home/vladi/Desktop/retos/reto/fixme2)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.10s
     Running `/home/vladi/Desktop/retos/reto/fixme2/target/debug/rust_proj main`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: picoCTF{4r3_y0u_h4v1n5_fun_y31?}
```
### Flag: picoCTF{4r3_y0u_h4v1n5_fun_y31?}
# Notas
Descomprimi el archivo con gzip y tar, adento venia un main.rs, lo ejecute con el comando cargo run. El compilador tiro errores de una variable &String, que estaba en lectura, lo arregle agregando una referencia mutable &mut String y agrege el mut a la variable en el resto del programa, compile y me dio la bandera.
# Referencias
https://doc.rust-lang.org/book/ch04-02-references-and-borrowing.html