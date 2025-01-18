Puedes asignar alias a los `middleware` de tu aplicación mediante el `boostratp.php` , te permiten definir un nombre corto a tus clases de `middleware`

```php
use App\Http\Middleware\EnsureUserIsSubscribed;
 
->withMiddleware(function (Middleware $middleware) {
    $middleware->alias([
        'subscribed' => EnsureUserIsSubscribed::class
    ]);
})
```

Una vez que lo hallas agregado lo puedes llamar desde `bootstrap/app.php`

```php
Route::get('/profile', function () {
    // ...
})->middleware('subscribed');
```

## Tags

##### #Laravel