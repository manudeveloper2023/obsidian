A menudo , no es tan necesario el `ID` del elemento principal como el del elemento secundario dentro de una `URI` , ya que el ID del elemento secundario ya es un identificador único.Por lo que , si no es necesario que el recurso secundario use al `recurso principal` para realizar operaciones , puedes usar el `shallow nesting`

```php
use App\Http\Controllers\CommentController;
 
Route::resource('photos.comments', CommentController::class)->shallow();
```

|Verb|URI|Action|Route Name|
|---|---|---|---|
|GET|`/photos/{photo}/comments`|index|photos.comments.index|
|GET|`/photos/{photo}/comments/create`|create|photos.comments.create|
|POST|`/photos/{photo}/comments`|store|photos.comments.store|
|GET|`/comments/{comment}`|show|comments.show|
|GET|`/comments/{comment}/edit`|edit|comments.edit|
|PUT/PATCH|`/comments/{comment}`|update|comments.update|
|DELETE|`/comments/{comment}`|destroy|comments.destroy|

## Tags

##### #Laravel
##### #Laravel-Controllers