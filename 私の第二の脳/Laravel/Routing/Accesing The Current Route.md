Puedes usar el **`current` , `curentRouteName` y `currentRouteAction`** para el método de fachada de `Route` para acceder a la informacion sobre la ruta que maneja la solicitud entrante

## Ejemplo

```php
use Illuminate\Support\Facades\Route;
 
$route = Route::current(); // Illuminate\Routing\Route
$name = Route::currentRouteName(); // string
$action = Route::currentRouteAction(); // string
```
## Tags

##### #Laravel