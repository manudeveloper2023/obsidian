Puedes asignar un grupo de **`middlewares`** y llamarlas mediante una llave , lo cual lo puedes realizar usando `appendToGroup` con tu `bootstrap/app.php`

## Ejemplos

```php
use App\Http\Middleware\First;
use App\Http\Middleware\Second;
 
->withMiddleware(function (Middleware $middleware) {
    $middleware->appendToGroup('group-name', [
        First::class,
        Second::class,
    ]);
 
    $middleware->prependToGroup('group-name', [
        First::class,
        Second::class,
    ]);
})

Route::get('/', function () {
    // ...
})->middleware('group-name');
 
Route::middleware(['group-name'])->group(function () {
    // ...
});
```

## Tags

##### #Laravel