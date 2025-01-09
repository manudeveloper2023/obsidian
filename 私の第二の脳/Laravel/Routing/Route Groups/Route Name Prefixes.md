Se puede utilizar para anteponer cada ruta nombrada del grupo con una cadena de prefijo.

## Ejemplo

```php
Route::name('admin.')->group(function () {
    Route::get('/users', function () {
        // Route assigned name "admin.users"...
    })->name('users');
});
```

## Tags

##### #Laravel