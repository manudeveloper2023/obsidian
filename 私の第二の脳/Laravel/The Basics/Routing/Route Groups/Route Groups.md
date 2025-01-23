Permiten que se puedan compartir los atributos de las rutas como los **`middlewares`** sin la necesidad de colocarlas en cada ruta individualmente

Por ejemplo , las propiedades de **`where`** y **`middleware`** son fusionadas , mientras se agregan los **`nombres`** y **`prefijos`**.Los delimitadores de espacios de nombres y las barras en los prefijos de la **URI** se agregan automáticamente cuando corresponde 

## Ejemplo


```php
Route::get('/user/{id}', function (string $id) {
    return response()->json([
        'id' => $id,
        'name' => 'John Doe',
        'email' => 'johndeo@gmail.com',
    ]);
})->where('id', '[0-9]+');
```
## Tags

##### #Laravel