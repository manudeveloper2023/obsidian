Laravel incluye `cache.headers` , que puedes usar para agregar un `Cache-Control header` para un grupo de rutas .

Las directivas deben proporcionarse utilizando el equivalente "snake case" de la `cache-control` correspondiente y deben estar separadas por un punto y coma.

Si se especifica `etag` en la lista de directivas , se configurará automáticamente un hash `MD5` del contenido de la respuesta

```php
Route::middleware('cache.headers:public;max_age=2628000;etag')->group(function () {
    Route::get('/privacy', function () {
        // ...
    });
 
    Route::get('/terms', function () {
        // ...
    });
});
```

## Tags

##### #Laravel
##### #Laravel-Response