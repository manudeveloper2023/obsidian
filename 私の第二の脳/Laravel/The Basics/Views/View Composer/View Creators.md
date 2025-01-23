Son muy similares a los [[View Composer]].Sin embargo , ellos son ejecutados despues de que la vista sea instanciada esperando hasta que la vista esté a punto de renderizarse

## Ejemplo


```php
namespace App\Http\View\Creators;

use Illuminate\View\View;
use App\Repositories\UserRepository;

class ProfileCreator
{
    protected UserRepository $users;

    /**
     * Crear una nueva instancia del view creator.
     */
    public function __construct(UserRepository $users)
    {
        $this->users = $users;
    }

    /**
     * Crear datos para la vista antes de que se cargue.
     */
    public function create(View $view): void
    {
        // Asignamos el número de usuarios antes de que la vista se cargue
        $view->with('count', $this->users->count());
    }
}
```

```php
namespace App\Providers;

use Illuminate\Support\ServiceProvider;
use Illuminate\Support\Facades\View;
use App\Http\View\Creators\ProfileCreator;

class AppServiceProvider extends ServiceProvider
{
    public function boot()
    {
        // Usamos View::creator() para registrar el creator para la vista 'profile'
        View::creator('profile', ProfileCreator::class);
    }

    public function register()
    {
        //
    }
}

```

```php
// ../resources/views/profile.blade.php

<h1>Profile</h1>
<p>There are {{ $count }} users in the system.</p>
```
## Tags

##### #Laravel
##### #Laravel-View