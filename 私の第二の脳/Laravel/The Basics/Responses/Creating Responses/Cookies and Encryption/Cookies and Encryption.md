Por defecto , `Laravel` encripta las `cookies` gracias al middleware de `Illuminate\Cookie\Middleware\EncryptCookies` , están cifradas y firmadas para que el cliente no pueda modificarlas ni leerlas

Si lo quiere deshabilitar puedes hacerlo mediante el método de `bootstrap/app.php`

```php
->withMiddleware(function (Middleware $middleware) {
    $middleware->encryptCookies(except: [
        'cookie_name',
    ]);
})
```
## Tags

##### #Laravel
##### #Laravel-Response