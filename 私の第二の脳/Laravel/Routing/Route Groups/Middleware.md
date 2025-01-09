Para asignar un **`middleware`** a todas las rutas dentro de un grupo , necesitaremos usar su método de facade de **`Route::middleware`** , los cuales son ejecutados en el orden del arreglo

## Ejemplo

```php
Route::middleware(['first', 'second'])->group(function () {
    Route::get('/', function () {
        // Uses first & second middleware...
    });
 
    Route::get('/user/profile', function () {
        // Uses first & second middleware...
    });
});
```
## Tags

##### #Laravel