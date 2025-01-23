Si estas utilizando `AWS` o otro cloud con un `ELB` , puedes no conocer la dirección IP de tus balanceadores de carga , en este caso puedes usar 

```php
->withMiddleware(function (Middleware $middleware) {
    $middleware->trustProxies(at: '*');
})
```
## Tags

##### #Laravel
##### #Laravel-Request