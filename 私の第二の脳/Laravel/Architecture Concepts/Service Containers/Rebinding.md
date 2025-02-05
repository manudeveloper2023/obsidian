Permite escuchar cuándo se `vuelve a vincular un servicio` al contenedor.

Lo cual es útil para `actualizar dependencias o modificar` el comportamiento cada vez que se actualiza una vinculación específica

```php
use App\Contracts\PodcastPublisher;
use App\Services\SpotifyPublisher;
use App\Services\TransistorPublisher;
use Illuminate\Contracts\Foundation\Application;
 
$this->app->bind(PodcastPublisher::class, SpotifyPublisher::class);
 
$this->app->rebinding(
    PodcastPublisher::class,
    function (Application $app, PodcastPublisher $newInstance) {
        //
    },
);
 
// New binding will trigger rebinding closure...
$this->app->bind(PodcastPublisher::class, TransistorPublisher::class);
```
### Tags
##### #Laravel 
##### #Laravel-Service-Containers