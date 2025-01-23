Se encargan de asignar a las vistas antes de que se renderizen , se pueden usar para datos que deben estar disponibles en varias vistas , puedes pasarlos sin tener que usar un controlador

Seran registrados en los `service providers` , para implementarlas en las vistas necesarias

## Ejemplo


```php
public function boot(): void
    {
        View::composer(
            'profile', // Vista donde se va a utilizar el composer
            ProfileComposer::class // La clase del composer
        );
 
        Facades\View::composer('dashboard', function (View $view) {
            // ...
        });
    }
```

Puedes crear una vista con el método de `compose` en `App\View\Composers\ProfileComposer`

```php
<?php
 
namespace App\View\Composers;
 
use App\Repositories\UserRepository;
use Illuminate\View\View;
 
class ProfileComposer
{
    /**
     * Create a new profile composer.
     */
    public function __construct(
        protected UserRepository $users,
    ) {}
 
    /**
     * Bind data to the view.
     */
    public function compose(View $view): void
    {
        $view->with('count', $this->users->count());
    }
}
```
## Tags

##### #Laravel
##### #Laravel-View
