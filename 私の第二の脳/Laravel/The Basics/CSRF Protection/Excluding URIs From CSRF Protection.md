
A veces tu quieres excluir un conjunto de `URIs` para el `CSRF protection`.Por ejemplo , si usas `Stripe` para procesar los pagos y estas utilizando un `webhook system`  , necesitar excluir la ruta de  `Stripe` , ya que Stripe no sabrá qué token CSRF enviar a tus rutas.

```php
->withMiddleware(function (Middleware $middleware) {
    $middleware->validateCsrfTokens(except: [
        'stripe/*',
        'http://example.com/foo/bar',
        'http://example.com/foo/*',
    ]);
})
```
## Tags

##### #Laravel
##### #Laravel-CSRF
