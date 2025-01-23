Estos crean un `CRUD` de rutas a un `controlador` con una simple linea de código

```bash
php artisan make:controller PhotoController --resource
```

Generara el controlador en `app/Http/Controllers/PhotoController.php` , con todos los métodos para el `CRUD` , ahora puedes registrar la ruta con `resource`

```php
use App\Http\Controllers\PhotoController;
 
Route::resource('photos', PhotoController::class);
```

Además , puedes pasar más de un controlador mediante `resources`


```php
Route::resources([
    'photos' => PhotoController::class,
    'posts' => PostController::class,
]);
```

#### [Actions Handled by Resource Controllers](https://laravel.com/docs/11.x/controllers#actions-handled-by-resource-controllers)

|Verb|URI|Action|Route Name|
|---|---|---|---|
|GET|`/photos`|index|photos.index|
|GET|`/photos/create`|create|photos.create|
|POST|`/photos`|store|photos.store|
|GET|`/photos/{photo}`|show|photos.show|
|GET|`/photos/{photo}/edit`|edit|photos.edit|
|PUT/PATCH|`/photos/{photo}`|update|photos.update|
|DELETE|`/photos/{photo}`|destroy|photos.destroy|
## Tags

##### #Laravel
##### #Laravel-Controllers