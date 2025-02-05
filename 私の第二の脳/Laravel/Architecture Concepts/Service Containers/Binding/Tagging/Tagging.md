Ocasionalmente , puede que necesites resolver todos los enlaces de una determinada `categoria`.Por ejemplo , realizar multiples `implementaciones de reporte` y registrarlas con un `tag`

```php
$this->app->bind(CpuReport::class, function () {
    // ...
});
 
$this->app->bind(MemoryReport::class, function () {
    // ...
});
 
$this->app->tag([CpuReport::class, MemoryReport::class], 'reports');
```

Una vez tageados , puedes `resolverlos` facilmente con a través del método `tagged`

```php
$this->app->extend(Service::class, function (Service $service, Application $app) {
    return new DecoratedService($service);
});
```

### Tags
##### #Laravel 
##### #Laravel-Service-Containers