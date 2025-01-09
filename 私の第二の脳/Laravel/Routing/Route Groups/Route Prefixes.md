Puede ser usado para anteponer un **`URI determinado`** a cada ruta del grupo

## Ejemplo

```php
Route::prefix('admin')->group(function () {
    Route::get('/users', function () {
        // Matches The "/admin/users" URL
    });
});
```
## Tags

##### #Laravel
