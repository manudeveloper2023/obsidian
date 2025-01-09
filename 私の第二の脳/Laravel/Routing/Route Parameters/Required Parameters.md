Algunas veces necesitaremos capturar segmentos de la **URI** con la ruta.Se inyectan según su orden en la ruta

## Ejemplo

```php
Route::get('/user/{id}', function (string $id) {
    return response()->json([
        'id' => $id,
        'name' => 'John Doe',
        'email' => 'johndeo@gmail.com',
    ]);
});
```

Puede definir tantos parametros como usted desee

```php
Route::get('/posts/{post}/comments/{comment}', function (string $postId, string $commentId) {
    // ...
});
```

## Tags

##### #Laravel