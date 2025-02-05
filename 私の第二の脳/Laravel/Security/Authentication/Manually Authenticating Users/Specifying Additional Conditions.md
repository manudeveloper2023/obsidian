También puedes añadir condiciones extra a la `query` de autenticación en adición al `email` y contraseña

```PHP

if (Auth::attempt(['email' => $email, 'password' => $password, 'active' => 1])) {
    // Authentication was successful...
}
```

Para `query` complejas puedes invocar un `Closure` con la `query`

```php
use Illuminate\Database\Eloquent\Builder;
 
if (Auth::attempt([
    'email' => $email,
    'password' => $password,
    fn (Builder $query) => $query->has('activeSubscription'),
])) {
    // Authentication was successful...
}
```

Puedes usar `attemptWhen` , que recibe un `Closure` como segundo argumento y realiza una inspección más exhaustiva

```php
if (Auth::attemptWhen([
    'email' => $email,
    'password' => $password,
], function (User $user) {
    return $user->isNotBanned();
})) {
    // Authentication was successful...
}
```
## Tags

##### #Laravel
##### #Laravel-Authentication