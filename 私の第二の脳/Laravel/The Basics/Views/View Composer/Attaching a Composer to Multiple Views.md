Puedes usar una `view composer` para pasar multiples vistas mediante un `arreglo de vistas` pasandolo como el `primer argumento de composer`

```php
use App\Views\Composers\MultiComposer;
use Illuminate\Support\Facades\View;
 
View::composer(
    ['profile', 'dashboard'],
    MultiComposer::class
);

// Si quieres pasarlas a todas tus vistas puedes usar

use Illuminate\Support\Facades;
use Illuminate\View\View;
 
Facades\View::composer('*', function (View $view) {
    // ...
});
```
## Tags

##### #Laravel
##### #Laravel-View
