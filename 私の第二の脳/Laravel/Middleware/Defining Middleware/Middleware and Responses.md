Un **middleware** puede realizar tareas antes o después de pasar la solicitud a un **`nivel más profundo de la aplicación`**

```php
<?php
 
namespace App\Http\Middleware;
 
use Closure;
use Illuminate\Http\Request;
use Symfony\Component\HttpFoundation\Response;
 
class BeforeMiddleware
{
    public function handle(Request $request, Closure $next): Response
    {
        // Perform action
 
        return $next($request);
    }
}
```

Sin embargo , este `middleware` ejecuta una tarea despues el petición 

```php
<?php
 
namespace App\Http\Middleware;
 
use Closure;
use Illuminate\Http\Request;
use Symfony\Component\HttpFoundation\Response;
 
class AfterMiddleware
{
    public function handle(Request $request, Closure $next): Response
    {
        $response = $next($request);
 
        // Perform action
 
        return $response;
    }
}
```
## Tags

##### #Laravel