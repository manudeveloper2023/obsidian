
El método de `Auth::attempt` te valida las credenciales que le has ofrecido , la `password` se hashea y se compara con el valor de la base de datos y retorna verdadero o falso

Los servicios de autenticación de `laravel` te otorgaran los usuarios en función del `provedor` que has asignado en `config/auth.php`

El método de `intended` provee una `redirección` a la ruta que querias acceder antes de que te hallan redireccionado a `login` para registrarte


```php
<?php
 
namespace App\Http\Controllers;
 
use Illuminate\Http\Request;
use Illuminate\Http\RedirectResponse;
use Illuminate\Support\Facades\Auth;
 
class LoginController extends Controller
{
    /**
     * Handle an authentication attempt.
     */
    public function authenticate(Request $request): RedirectResponse
    {
        $credentials = $request->validate([
            'email' => ['required', 'email'],
            'password' => ['required'],
        ]);
 
        if (Auth::attempt($credentials)) {
            $request->session()->regenerate();
 
            return redirect()->intended('dashboard');
        }
 
        return back()->withErrors([
            'email' => 'The provided credentials do not match our records.',
        ])->onlyInput('email');
    }
}
```
## Tags

##### #Laravel
##### #Laravel-Authentication