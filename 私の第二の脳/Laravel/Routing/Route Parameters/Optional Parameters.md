Si tu quieres crear un parámetro que sea opcional deberas que colocar **`?`** despues del nombre del parámetro

## Ejemplo

```php
Route::get('/user/{name?}', function (?string $name = null) {
    return $name;
});
 
Route::get('/user/{name?}', function (?string $name = 'John') {
    return $name;
});
```

## Tags

##### #Laravel