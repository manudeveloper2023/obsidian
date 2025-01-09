Se pueden utilizar para el gestionamiento de **enrutamiento de los subdominios**.Se les puede asignar parámetros de ruta al igual que a las **URL de ruta** , lo que permite **`capturar una parte del subdominio`**.Mediante el método de **`Route::domain`**


```php
Route::domain('{account}.example.com')->group(function () {
    Route::get('/user/{id}', function (string $account, string $id) {
        // ...
    });
});
```

## Tags

##### #Laravel