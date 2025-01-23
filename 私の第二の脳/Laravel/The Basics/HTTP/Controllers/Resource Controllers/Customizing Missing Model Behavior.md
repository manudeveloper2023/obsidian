Puedes customizar la `HTTP Response 404` llamando al método de `missing` cuando definas los recursos de tu ruta.En caso que no encuentre un recurso en específico activara a este método de `missing`

## Ejemplo


```php
use App\Http\Controllers\PhotoController;
use Illuminate\Http\Request;
use Illuminate\Support\Facades\Redirect;
 
Route::resource('photos', PhotoController::class)
        ->missing(function (Request $request) {
            return Redirect::route('photos.index');
        });
```
## Tags

##### #Laravel
##### #Laravel-Controllers