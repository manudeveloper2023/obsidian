La mayoria de los `service containers bindings` seran registrados en el `service providers`

Dentro de un `service provider` , siempre puedes acceder al contenedor a través de la propiedad `$this->app`.Puedes registrar un enlace usando el `bind method` 

```php
use App\Services\Transistor;
use App\Services\PodcastParser;
use Illuminate\Contracts\Foundation\Application;
 
$this->app->bind(Transistor::class, function (Application $app) {
    return new Transistor($app->make(PodcastParser::class));
});
```

Si quieres interactuar con el contenedor `fuera del service provider` puedes usar la fachada de `App`

```php
use App\Services\Transistor;
use Illuminate\Contracts\Foundation\Application;
use Illuminate\Support\Facades\App;
 
App::bind(Transistor::class, function (Application $app) {
    // ...
});
```

Para evitar que un `binding` se sobreescriba si ya existe un `binding` se usa `bindingIf`

```php
$this->app->bindIf(Transistor::class, function (Application $app) {
    return new Transistor($app->make(PodcastParser::class));
});
```

> No es necesario `vincular clases` al contenedor si no dependen de ninguna interfaz, ya que el contenedor ya puede resolverlos automáticamente usando reflexión
### Tags
##### #Laravel 
##### #Laravel-Service-Containers