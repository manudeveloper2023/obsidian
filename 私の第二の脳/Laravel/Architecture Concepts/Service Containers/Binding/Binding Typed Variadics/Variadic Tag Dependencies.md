A veces una clase puede tener una `dependencia variadica` que cuyo tipo se indica como una `clase determinada(Report ...$reports)`.

Con los métodos de `needs` y `giveTagged` , puedes inyectar fácilmente todos los enlaces de contenedor con esta etiqueta para la dependencia determinada

```php
$this->app->when(ReportAggregator::class)
    ->needs(Report::class)
    ->giveTagged('reports');
```
### Tags
##### #Laravel 
##### #Laravel-Service-Containers