Puedes crear tus propios `contextual attributes` implementado el `Illuminate\Contracts\Container\ContextualAttribute`.El contenedor llamará al método `resolve` del atributo, que debería devolver el valor que se debe inyectar a la clase que use el atributo

```php
<?php
 
namespace App\Attributes;
 
use Illuminate\Contracts\Container\ContextualAttribute;
 
#[Attribute(Attribute::TARGET_PARAMETER)]
class Config implements ContextualAttribute
{
    /**
     * Create a new attribute instance.
     */
    public function __construct(public string $key, public mixed $default = null)
    {
    }
 
    /**
     * Resolve the configuration value.
     *
     * @param  self  $attribute
     * @param  \Illuminate\Contracts\Container\Container  $container
     * @return mixed
     */
    public static function resolve(self $attribute, Container $container)
    {
        return $container->make('config')->get($attribute->key, $attribute->default);
    }
}
```
### Tags
##### #Laravel 
##### #Laravel-Service-Containers