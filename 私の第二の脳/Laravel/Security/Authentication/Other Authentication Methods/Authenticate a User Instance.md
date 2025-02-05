Si necesitas establecer una instancia de usuario existente como usuario autenticado , puedes pasar la instancia de fachada de `login` para autenticarlo , que debe tener la interfaz de `Illuminate\Contracts\Auth\Authenticatable`

Se suele usar para autenticar al usuario después de registrarse 

```php
use Illuminate\Support\Facades\Auth;
 
Auth::login($user);
```
 
Puedes pasar un segundo argumento booleano , con el `remember` para la sesión autenticada

```php
Auth::login($user, $remember = true);
```

Si necesitas específicar un `guard` antes de llamar al método de inicio de sesión

```php
Auth::guard('admin')->login($user);
```
## Tags

##### #Laravel
##### #Laravel-Authentication