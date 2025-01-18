`Laravel` genera un `CSRF token` por cada sesión de usuario activa manejada por la aplicación.Este token es utilizado para verificar que el usuario autenticado esta creando actualmente los `requests` en la aplicación

Dado que este `token` se almacena en la sesión del usuario y cambia cada vez que se regenera la sesión , para que una aplicación maliciosa no pueda acceder a él.

El `csrf_token` actual se puede acceder via el `request session` o via la función helper de `csrf_token()`

```php
use Illuminate\Http\Request;
 
Route::get('/token', function (Request $request) {
    $token = $request->session()->token();
 
    $token = csrf_token();
 
    // ...
});
```

Cada vez que definas un `POST` , `PUT` , `PATH` o `DELETE` en un formulario HTML en tu aplicación , deberias incluir un `CSRF token` escondido en el `field` que el `CSRF middleware` puede validar la solicitud.

Por conveniencia , puedes usar la directiva de `@csrf` para generar el token escondido en el `input field`

```php
<form method="POST" action="/profile">
    @csrf
 
    <!-- Equivalent to... -->
    <input type="hidden" name="_token" value="{{ csrf_token() }}" />
</form>
```

El `Illuminate\Foundation\Http\Middleware\ValidateCsrfToken` , es un `middelware` que se incluye en el grupo de `web` por defecto , automaticamente verificara que el `token` en el `request input` coincide con el `token` almacenado en sesión.Cuando estos dos tokens coincidan , ellos sabran que el usuario `autenticado` esta iniciando el `request`

## Tags

##### #Laravel
##### #Laravel-CSRF