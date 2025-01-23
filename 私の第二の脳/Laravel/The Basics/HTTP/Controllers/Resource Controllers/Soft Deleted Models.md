Indica que las rutas del recurso deben incluir también las fotos con las que realizaron `soft deleted` para las consultas

## Ejemplo


```php
use App\Http\Controllers\PhotoController;
 
Route::resource('photos', PhotoController::class)->withTrashed();
```

Puedes específicar un subconjunto de las rutas pasando un arreglo al método de `withTrashed`

```php
Route::resource('photos', PhotoController::class)->withTrashed(['show']);
```

## Tags

##### #Laravel
##### #Laravel-Controllers