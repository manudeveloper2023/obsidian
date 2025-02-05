Puedes vincular una instancia de un objeto existente al contenedor mediante el método de `instance`

La instancia dada siempre se`devolverá` en las llamadas posteriores al contenedor

Es util cuando ya tienes una instancia `creada` y quieres compartirla en todo el contenedor

```php
use App\Services\Transistor;
use App\Services\PodcastParser;
 
$service = new Transistor(new PodcastParser);
 
$this->app->instance(Transistor::class, $service);
```
### Tags
##### #Laravel 
##### #Laravel-Service-Containers