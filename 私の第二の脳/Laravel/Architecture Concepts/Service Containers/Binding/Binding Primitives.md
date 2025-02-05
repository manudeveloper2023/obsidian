A veces puedes tener una clase que reciba algunas `clases inyectadas` , pero también necesite un valor primitivo inyectado , como un entero

```php
use App\Http\Controllers\UserController;
 
$this->app->when(UserController::class)
          ->needs('$variableName')
          ->give($value);
```

A veces , una clase puede depender de una matriz de instancias etiquetadas

```php
$this->app->when(ReportAggregator::class)
    ->needs('$reports')
    ->giveTagged('reports');
```

Si necesitas inyectar un valor desde uno de los archivos de configuración de su aplicación , puede utilizar el método `giveConfig`

```php
$this->app->when(ReportAggregator::class)
    ->needs('$timezone')
    ->giveConfig('app.timezone');
```
### Tags
##### #Laravel 
##### #Laravel-Service-Containers