Cuando delcares una ruta de recursos , puedes especificar un `subgrupo de acciones` que el controlador deberia manejar 

```php
use App\Http\Controllers\PhotoController;
 
Route::resource('photos', PhotoController::class)->only([
    'index', 'show'
]);
 
Route::resource('photos', PhotoController::class)->except([
    'create', 'store', 'update', 'destroy'
]);
```
## Tags

##### #Laravel
##### #Laravel-Controllers