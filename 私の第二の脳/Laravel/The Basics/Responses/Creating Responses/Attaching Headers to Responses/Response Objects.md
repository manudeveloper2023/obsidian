Devolver una instancia de `response` permite personalizar el estado del código HTTP y los encabezados de una respuesta

```php
Route::get('/home', function () {
    return response('Hello World', 200)
                  ->header('Content-Type', 'text/plain');
});
```
## Tags

##### #Laravel
##### #Laravel-Response