Cuando adjuntes la ruta `de middleware` puedes , especificar que `guard` debes que usar con el usuario autenticado

```php
Route::get('/flights', function () {
    // Only authenticated users may access this route...
})->middleware('auth:admin');
```
## Tags

##### #Laravel
##### #Laravel-Authentication
