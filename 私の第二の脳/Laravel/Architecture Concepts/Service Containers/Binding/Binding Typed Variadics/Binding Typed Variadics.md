Puedes tener una clase que reciba un arreglo de objetos tipificados utilizando un argumento de constructor variádico

```php
<?php
 
use App\Models\Filter;
use App\Services\Logger;
 
class Firewall
{
    /**
     * The filter instances.
     *
     * @var array
     */
    protected $filters;
 
    /**
     * Create a new class instance.
     */
    public function __construct(
        protected Logger $logger,
        Filter ...$filters,
    ) {
        $this->filters = $filters;
    }
}
```

Usando `contextual binding` , puedes resolver esta dependencia con el método de `give` con un `closure` que retorna un arreglo de `instancias de Filter resueltos`

```php
$this->app->when(Firewall::class)
          ->needs(Filter::class)
          ->give(function (Application $app) {
                return [
                    $app->make(NullFilter::class),
                    $app->make(ProfanityFilter::class),
                    $app->make(TooLongFilter::class),
                ];
          });
```

Por conveniencia , también puedes resolverlas con una matriz de nombres de clases siempre que `Firewall` necesite las instancia de filtro

```php
$this->app->when(Firewall::class)
          ->needs(Filter::class)
          ->give([
              NullFilter::class,
              ProfanityFilter::class,
              TooLongFilter::class,
          ]);
```
### Tags
##### #Laravel 
##### #Laravel-Service-Containers