Un `middleware` puede ser asignado a un `controlador de rutas` en tus archivos de rutas

```php
Route::get('/profile', [UserController::class, 'show'])->middleware('auth');
```

O puede agregarlos dentro del controlador implementando la interfaz de `HasMiddleware` , mediante el método estático de `middleware`

```php
<?php
 
namespace App\Http\Controllers;
 
use App\Http\Controllers\Controller;
use Illuminate\Routing\Controllers\HasMiddleware;
use Illuminate\Routing\Controllers\Middleware;
 
class UserController extends Controller implements HasMiddleware
{
    /**
     * Get the middleware that should be assigned to the controller.
     */
    public static function middleware(): array
    {
        return [
            'auth',
            new Middleware('log', only: ['index']),
            new Middleware('subscribed', except: ['store']),
        ];
    }
 
    // ...
}
```

Además , puedes definir un `middleware` mediante `closures` , que proporciona una forma conveniente de definir un `middleware` sin su clase

```php
use Closure;
use Illuminate\Http\Request;
 
/**
 * Get the middleware that should be assigned to the controller.
 */
public static function middleware(): array
{
    return [
        function (Request $request, Closure $next) {
            return $next($request);
        },
    ];
}
```

## Tags

##### #Laravel
##### #Laravel-Controllers