Estos los podemos usar en `web` y `api` en el `boostratp/app.php`

## Ejemplo

```php
use App\Http\Middleware\EnsureTokenIsValid;
use App\Http\Middleware\EnsureUserIsSubscribed;
 
->withMiddleware(function (Middleware $middleware) {
    $middleware->web(append: [
        EnsureUserIsSubscribed::class,
    ]);
 
    $middleware->api(prepend: [
        EnsureTokenIsValid::class,
    ]);
})
```

Además , puedes reemplazar uno de los `middleware` por defecto de Laravel con un `middleware propio`

```php
use App\Http\Middleware\StartCustomSession;
use Illuminate\Session\Middleware\StartSession;
 
$middleware->web(replace: [
    StartSession::class => StartCustomSession::class,
]);
```

Y también los puedes **`eliminar`**

```php
$middleware->web(remove: [
    StartSession::class,
]);
```
## Tags

##### #Laravel