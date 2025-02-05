Para cerrar las sesiones de la aplicación manualmente , puedes utilizar el método de `logout`.Esto eliminará la información de autenticación de la sesión del usuario para que solicitudes posteriores no se `autentiquen`

```php
use Illuminate\Http\Request;
use Illuminate\Http\RedirectResponse;
use Illuminate\Support\Facades\Auth;
 
/**
 * Log the user out of the application.
 */
public function logout(Request $request): RedirectResponse
{
    Auth::logout();
 
    $request->session()->invalidate();
 
    $request->session()->regenerateToken();
 
    return redirect('/');
}
```

## Tags

##### #Laravel
##### #Laravel-Authentication