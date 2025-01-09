Por defecto , el middleware de **`throttle`** es mapeado para la clase **`Illuminate\Routing\Middleware\ThrottleRequests`**.Sin embargo , si estas usando **Redis** para tu aplicación , puedes indicarle a Laravel que utilice Redis para administrar la limitación de velocidad.Utilizando el método de **`throttleWithRedis`** en el archivo `bootstrap/app.php`

## Ejemplo

```php
->withMiddleware(function (Middleware $middleware) {
    $middleware->throttleWithRedis();
    // ...
})
```
## Tags

##### #Laravel