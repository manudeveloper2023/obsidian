
Si quiere permitir que el caracter **`/`** se permita usar como un parámetro puedes usar la condicion de **`where`** con una expresión regular

```php
Route::get('/search/{search}', function (string $search) {
    return $search;
})->where('search', '.*');
```

## Tags

##### #Laravel