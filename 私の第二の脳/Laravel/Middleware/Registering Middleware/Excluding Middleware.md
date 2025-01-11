Cuando asignes un **`middleware`** a un grupo de rutas , puedes ocasionalmente evitar que el middleware se aplique a una ruta individual dentro del grupo.

## Ejemplo


```php
use App\Http\Middleware\EnsureTokenIsValid;
 
Route::middleware([EnsureTokenIsValid::class])->group(function () {
    Route::get('/', function () {
        // ...
    });
 
    Route::get('/profile', function () {
        // ...
    })->withoutMiddleware([EnsureTokenIsValid::class]);
});
```

Puedes excluirlos en un conjunto determinado de middlewares de un grupo completo de definiciones de ruta 

```php
use App\Http\Middleware\EnsureTokenIsValid;
 
Route::withoutMiddleware([EnsureTokenIsValid::class])->group(function () {
    Route::get('/profile', function () {
        // ...
    });
});
```
## Tags

##### #Laravel
