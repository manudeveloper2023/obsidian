
Si tu quieres asignar un **`middleware`** a unas rutas específicas , lo puedes hacer mediante el método de **`->middleware()`**

## Ejemplo

```php
use App\Http\Middleware\EnsureTokenIsValid;
 
Route::get('/profile', function () {
    // ...
})->middleware(EnsureTokenIsValid::class);
```

Si quiere asignar mas de uno , puede agregarlos en un arreglo

```php
Route::get('/', function () {
    // ...
})->middleware([First::class, Second::class]);
```
## Tags

##### #Laravel
