El método de `scope` vincula una clase o interfaz al contenedor que solo debe resolverse una vez `dentro de un ciclo de vida de solicitud o trabajos de Laravel`

Las instancias de `scoped` se eliminaran una vez que la aplicación de `Laravel` inicia un nuevo `"ciclo de vida"` 

```php
use App\Services\Transistor;
use App\Services\PodcastParser;
use Illuminate\Contracts\Foundation\Application;
 
$this->app->scoped(Transistor::class, function (Application $app) {
    return new Transistor($app->make(PodcastParser::class));
});
```

Puedes usar `scopedIf` para registrar un enlace de contenedor con ámbito solo si aún no se ha `registrado un enlace para el tipo dado`

```PHP
$this->app->scopedIf(Transistor::class, function (Application $app) {
    return new Transistor($app->make(PodcastParser::class));
});
```

### Tags
##### #Laravel 
##### #Laravel-Service-Containers