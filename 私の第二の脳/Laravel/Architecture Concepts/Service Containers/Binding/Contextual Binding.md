A veces puedes tener dos clases que utilizan la misma interfaz , pero deseas inyectar `diferentes implementaciones en cada clase`


## Ejemplo

Tienes dos controladores que dependan de diferentes implementaciones de `Illuminate\Contracts\Filesystem\Filesystem`


```php
use App\Http\Controllers\PhotoController;
use App\Http\Controllers\UploadController;
use App\Http\Controllers\VideoController;
use Illuminate\Contracts\Filesystem\Filesystem;
use Illuminate\Support\Facades\Storage;
 
$this->app->when(PhotoController::class)
          ->needs(Filesystem::class)
          ->give(function () {
              return Storage::disk('local');
          });
 
$this->app->when([VideoController::class, UploadController::class])
          ->needs(Filesystem::class)
          ->give(function () {
              return Storage::disk('s3');
          });
```

### Tags
##### #Laravel 
##### #Laravel-Service-Containers