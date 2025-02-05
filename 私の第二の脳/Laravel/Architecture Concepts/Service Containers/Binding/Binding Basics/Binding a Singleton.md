Vincula una clase o interfaz  al contenedor que solo `se debe resolver una vez`

Una vez que se resuelve el enlace se devolverá la misma instancia de objeto en las llamadas posteriores

```php
use App\Services\Transistor;
use App\Services\PodcastParser;
use Illuminate\Contracts\Foundation\Application;
 
$this->app->singleton(Transistor::class, function (Application $app) {
    return new Transistor($app->make(PodcastParser::class));
});
```

También puede usar `singletonIf` para registrar un enlace de contenedor `Singleton` si no se ha registrado un enlace para el tipo dado

```php
$this->app->singletonIf(Transistor::class, function (Application $app) {
    return new Transistor($app->make(PodcastParser::class));
});
```
### Tags
##### #Laravel 
##### #Laravel-Service-Containers