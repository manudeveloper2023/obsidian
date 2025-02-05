Si el `Form Request Validation` falla , se generara una redirección para enviar al usuario de vuelta a su ubicación anterior

```PHP
/**
 * The URI that users should be redirected to if validation fails.
 *
 * @var string
 */
protected $redirect = '/dashboard';
```

O , si los desea redirigir a los usuarios a una ruta con nombre , puede redefinirlo con 

```php
/**
 * The route that users should be redirected to if validation fails.
 *
 * @var string
 */
protected $redirectRoute = 'dashboard';
```
## Tags

##### #Laravel
##### #Laravel-Validation