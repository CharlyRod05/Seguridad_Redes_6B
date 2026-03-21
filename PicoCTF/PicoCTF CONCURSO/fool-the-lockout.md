# Reto: Fool the Lockout

## Descripción

Your friend is building a simple website with a login page.
To stop brute forcing and credential stuffing, they’ve added an IP-based rate limit: exceed the attempt threshold and your IP is blocked for a while. They’re convinced this makes guessing credentials impossible.

To test their defense, they’ve:
- Created a dummy account with a random username–password pair from public credential lists.
- Given you those username and password lists.
- Shared the full source code.

## Solución

Lo bueno de tener el código es que podemos ver la lógica detrás de checar y bloquear las peticiones. Primero intenté cambiar mi ip en cada petición para intentar engañar a la web, pero parece que el servidor checa la IP de una forma que esto no es posible.

Un enfoque más 'simple' es el de simplemente ir con fuerza bruta. El server te limita a 10 peticiones cada 30 segundos, lo que podemos hacer es mandar esas 10 peticiones, esperar 30 segundos a la siguiente, mandar las siguientes 10 y así. Este es un enfoque posible sólo porque sólo se nos dieron 99 contraseñas a probar.

Ejecutamos el archivo `brute_force.py` que está en esta misma carpeta y esperando un poco logramos pasar.

`picoCTF{f00l_7h4t_l1m1t3r_24180dc6}`
