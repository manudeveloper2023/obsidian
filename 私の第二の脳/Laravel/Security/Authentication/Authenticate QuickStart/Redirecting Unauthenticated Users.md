Cuando el `auth` middleware detecte un usuario no autenticado , puedes redirigirlo a `cualquier ruta` con el método de `redirectGuestTo` con `bootstrap/app.php`

```php
use Illuminate\Http\Request;
 
->withMiddleware(function (Middleware $middleware) {
    $middleware->redirectGuestsTo('/login');
 
    // Using a closure...
    $middleware->redirectGuestsTo(fn (Request $request) => route('login'));
})
```
## Tags

##### #Laravel
##### #Laravel-Authentication