El método de `extend` permite la modificación de los `servicios resueltos`.Por ejemplo , cuando un servicio es resuelto, puedes correr un codigo adicional para decorarlo o configurarlo

Acepta dos argumentos el `servicio` que está extendiendo y un cierre que debe devolver el servicio modificado

```php
$this->app->extend(Service::class, function (Service $service, Application $app) {
    return new DecoratedService($service);
});
```
### Tags
##### #Laravel 
##### #Laravel-Service-Containers