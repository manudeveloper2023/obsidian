Puedes usar rutas que sean consumidas por `rutas` , puedes crearlas mediante `apiResource` , excluyendo los métodos de `create` y `edit`

## Ejemplo


```php
use App\Http\Controllers\PhotoController;
 
Route::apiResource('photos', PhotoController::class);
```

Si usaras muchas rutas de recursos mediante `API` , puedes usar un `array` con `ApiResources`

```php
use App\Http\Controllers\PhotoController;
use App\Http\Controllers\PostController;
 
Route::apiResources([
    'photos' => PhotoController::class,
    'posts' => PostController::class,
]);
```

Además , puedes crear un controlador con `--api` para editar los métodos de `edit` y `create`

```php
php artisan make:controller PhotoController --api
```
## Tags

##### #Laravel
##### #Laravel-Controllers