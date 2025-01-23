Para obtener la instancia de `HTTP` de rquest se usa via `DIP` , tu deberias poder usarlo con `Illuminate\Http\Request` , siendo automáticamente inyectado por el `service container`

```php
<?php
 
namespace App\Http\Controllers;
 
use Illuminate\Http\RedirectResponse;
use Illuminate\Http\Request;
 
class UserController extends Controller
{
    /**
     * Store a new user.
     */
    public function store(Request $request): RedirectResponse
    {
        $name = $request->input('name');
 
        // Store the user...
 
        return redirect('/users');
    }
}
```
## Tags

##### #Laravel
##### #Laravel-Request
