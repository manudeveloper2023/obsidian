```php
Route::get($uri, $callback);
Route::post($uri, $callback);
Route::put($uri, $callback);
Route::patch($uri, $callback);
Route::delete($uri, $callback);
Route::options($uri, $callback);
```

A veces crearas una ruta que responda muchos verbos **HTTP**.Por lo que podrias usar **`match`** , o si quieres registrar todos los metodos puedes usar **`any`**

```php
Route::match(['get', 'post'], '/', function () {
    // ...
});
 
Route::any('/', function () {
    // ...
});
```