# reto
# Descripción

Can you conjure the right bytes? The program's source code can be downloaded [here](https://challenge-files.picoctf.net/c_foggy_cliff/7c2e3cc6f15d9d2a6e5d78891b8a22d9bf4c79ac419d69341620edf09a35771d/app.py).Connect to the program with netcat:`$ nc foggy-cliff.picoctf.net 60705`

# Solución 
## solución
```
try: print('⊹──────[ BYTEMANCY-1 ]──────⊹') print("☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐") print() print('Send me ASCII DECIMAL 101 1751 times, side-by-side, no space.') print() print("☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐☉⟊☽☈⟁⧋⟡☍⟐") print('⊹─────────────⟡─────────────⊹') user_input = input('==> ') if user_input == "\x65"*1751: print(open("./flag.txt", "r").read()) break else: print("That wasn't it. I got: " + str(user_input)) print() print() print() except Exception as e: print(e) break
```
se nos da el codigo de arriba, lo que nos dice que el codigo ascii en 101 seria la "e", esta se tiene que ingresara 1751 veces de manera continua

python3 -c "print('e'*1751)" | nc foggy-cliff.picoctf.net 50814

dando la bandera siguiente
picoCTF{h0w_m4ny_e's???_62edb104}

## solución 2




# referencias

