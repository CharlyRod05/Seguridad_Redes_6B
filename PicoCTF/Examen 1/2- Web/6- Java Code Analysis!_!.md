**Descripció** 
BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!

Additional details will be available after launching your challenge instance.
**Solucion:** 

- Logear con las credenciales que indica
- Abrir herramientas de desarrollador
- Copiar el JWT(auth-token) desde Storage/Local Storage/http..
-  Pegar en [jwt.io](https://jwt.io/).
 - Editar el payload:
    
    { "id": 2, 
    "email": "admin", 
    "role": "Admin", ... }
    
-  Firmar con el secreto `1234`
- Obtener el nuevo JWT codificado
- Sustituir el JWT en Local Storage y asegurarse de que tambien editar el token-payload con los nuevos valores![[Pasted image 20260327140707.png]]
-  Refrescar la página y abrir el libro _Flag_.
**Flag** picoCTF{w34k_jwt_n0t_g00d_d72df65e}