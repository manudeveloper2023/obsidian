Si alguno de tus dependencias de clases no se pueden resolver a través del contenedor  puede inyectarlas pasándolas como una matriz asociativa con el método de `makeWith`

```php
use App\Services\Transistor;
 
$transistor = $this->app->makeWith(Transistor::class, ['id' => 1]);
```
### Tags
##### #Laravel 
##### #Laravel-Service-Containers