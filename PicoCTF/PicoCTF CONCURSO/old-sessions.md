# Reto: Old Sessions

## Descripción

Proper session timeout controls are critical for securing user accounts. If a user logs in on a public or shared computer but doesn’t explicitly log out (instead simply closing the browser tab), and session expiration dates are misconfigured, the session may remain active indefinitely.
This then allows an attacker using the same browser later to access the user’s account without needing credentials, exploiting the fact that sessions never expire and remain authenticated.

## Solución

Se nos presenta una página de inicio de sesión. Primero procedemos de forma normal, creando una cuenta y accediendo al portal. Hay varios comentarios, el más importante siendo uno mencionando la ruta `/sessions`.

Visitamos la página en la ruta `/sessions`. Hay dos, la nuestra y una que pertenece a un usuario `admin`. Simplemente cambiamos nuestra cookie por esta del admin y se nos da la flag.

`picoCTF{s3t_s3ss10n_3xp1rat10n5_10f20509}`
