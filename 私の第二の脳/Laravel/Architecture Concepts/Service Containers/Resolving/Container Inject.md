Si quieres inyectar el `Container` en la clase , puede escribir la clase de `Illuminate\Container\Container` en el constructor de la clase

```php
use Illuminate\Container\Container;
 
/**
 * Create a new class instance.
 */
public function __construct(
    protected Container $container,
) {}
```
### Tags
##### #Laravel 
##### #Laravel-Service-Containers