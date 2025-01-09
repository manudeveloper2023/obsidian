Son utiles para proporcionar funciones que nos ayudaran a nuestras clases.**Sin embargo**, debemos que evitar que la clase que poseemos se acople de muchas dependencais

## Ejemplo

```php
use Illuminate\Support\Facades\Cache;
use Illuminate\Support\Facades\Route;
 
Route::get('/cache', function () {
    return Cache::get('key');
});
```

## Tags

##### #Laravel