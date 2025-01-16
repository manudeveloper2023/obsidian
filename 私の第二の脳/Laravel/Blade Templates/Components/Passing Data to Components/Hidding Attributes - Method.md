Si quieres prevenir que los métodos públicos sean expuestos como variables al `template` del componente , puedes añadir `$except` para la propiedad de tu componente

```php
<?php
 
namespace App\View\Components;
 
use Illuminate\View\Component;
 
class Alert extends Component
{
    /**
     * The properties / methods that should not be exposed to the component template.
     *
     * @var array
     */
    protected $except = ['type'];
 
    /**
     * Create the component instance.
     */
    public function __construct(
        public string $type,
    ) {}
}
```
## Tags

##### #Laravel