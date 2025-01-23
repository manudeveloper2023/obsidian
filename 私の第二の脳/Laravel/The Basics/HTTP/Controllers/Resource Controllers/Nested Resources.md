A veces necesitas definir rutas para un recurso compartido.Por ejemplo , una foto puede tener muchos comentarios

```php
use App\Http\Controllers\PhotoCommentController;
 
Route::resource('photos.comments', PhotoCommentController::class);
```

Registrar esta ruta

```php
/photos/{photo}/comments/{comment}
```
## Tags

##### #Laravel
##### #Laravel-Controllers