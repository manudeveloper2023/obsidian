Puede acceder al usuario autenticado a través del método de `user`

```php
use Illuminate\Support\Facades\Auth;
 
// Retrieve the currently authenticated user...
$user = Auth::user();
 
// Retrieve the currently authenticated user's ID...
$id = Auth::id();
```

También , puedes acceder mediante `request->user()`

```PHP
public function update(Request $request): RedirectResponse
    {
        $user = $request->user();
 
        // ...
 
        return redirect('/flights');
    }
```
## Tags

##### #Laravel
##### #Laravel-Authentication
