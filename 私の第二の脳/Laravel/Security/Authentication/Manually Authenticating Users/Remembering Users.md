Muchas aplicaciones proporcionan una casilla de `recuerdame`.Si deseas proporcionar la función de recuérdame en su aplicación , como un segundo parametro booleano en `attempt`

Si este valor es verdadero , `Laravel` mantendrá autenticado al usuario indefinidamente o hasta que cierre la sesión

Que generara un `remember_token` en `User` que nos permite que estemos autenticados sin iniciar sesión nuevamente aunque cierres el navegador

```php
use Illuminate\Support\Facades\Auth;
 
if (Auth::attempt(['email' => $email, 'password' => $password], $remember)) {
    // The user is being remembered...
}
```

Puedes veríficar mediante el método de `viaRemember` para determinar si el usuario fue autenticado usando la cookie `remember`

```php
use Illuminate\Support\Facades\Auth;
 
if (Auth::viaRemember()) {
    // ...
}
```
## Tags

##### #Laravel
##### #Laravel-Authentication