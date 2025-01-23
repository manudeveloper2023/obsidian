Se pueden adjuntar limitadores de velocidad a rutas o grupos de rutas mediante el middleware de aceleración , además acepta el nombre del limitador de velocidad que desea asignar a la ruta

```php
Route::middleware(['throttle:uploads'])->group(function () {
    Route::post('/audio', function () {
        // ...
    });
 
    Route::post('/video', function () {
        // ...
    });
});
```

## Tags

##### #Laravel