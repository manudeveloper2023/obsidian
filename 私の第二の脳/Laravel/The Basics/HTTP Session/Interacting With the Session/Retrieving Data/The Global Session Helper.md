Si puedes usar la función helper de `session`.Cuando lo llames , puedes retornar el valor de esa `session key`.

```php
Route::get('/home', function () {
    // Retrieve a piece of data from the session...
    $value = session('key');
 
    // Specifying a default value...
    $value = session('key', 'default');
 
    // Store a piece of data in the session...
    session(['key' => 'value']);
});
```
## Tags

##### #Laravel
##### #Laravel-Session