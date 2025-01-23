Si tu componente requiere dependecias de un `service container` , tu puedes enumerarlas antes de cualquier de los atributos de los datos del componente y la inyectará automáticamente

```php
use App\Services\AlertCreator;
 
/**
 * Create the component instance.
 */
public function __construct(
    public AlertCreator $creator,
    public string $type,
    public string $message,
) {}
```

## Tags

##### #Laravel
