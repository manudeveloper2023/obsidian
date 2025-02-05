Puedes validar las rutas solo para usuarios autenticados `mediante el Illuminate\Auth\Middleware\Authenticate`

```php
Route::get('/flights', function () {
    // Only authenticated users may access this route...
})->middleware('auth');
```
## Tags

##### #Laravel
##### #Laravel-Authentication