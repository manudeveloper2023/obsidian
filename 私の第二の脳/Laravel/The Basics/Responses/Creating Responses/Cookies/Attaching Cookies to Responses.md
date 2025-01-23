Puedes unir una cookie al `response` usando el método de `cookie`

```php
return response('Hello World')->cookie(
    'name', 'value', $minutes, $path, $domain, $secure, $httpOnly
);
```

Si quieres enviar la cookie con la respuesta saliente pero aún no se crea , la puedes agregar en una `cola` para adjuntarlas cuando se envie

```php
use Illuminate\Support\Facades\Cookie;
 
Cookie::queue('name', 'value', $minutes);
```
## Tags

##### #Laravel
##### #Laravel-Response