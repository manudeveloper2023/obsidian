Laravel resuelve automáticamaente los modelos de **Eloquent** definidos en ruats o acciones de controlador cuyos nombres de variables con **`indicación de tipo coinciden con el nombre de un segmento de la ruta`**

## Ejemplo

Buscara el identificador del usuario usando el metodo de **`User::find(id)`** , lo cual lo inyectara en el parámetro **`$user`** si es que existe

Si no lo encuentra aparecera un error **`404 HTTP`** 

```php
use App\Models\User;
 
Route::get('/users/{user}', function (User $user) {
    return $user->email;
});
```

También es posible mediante un controlador

```php
use App\Http\Controllers\UserController;
use App\Models\User;
 
// Route definition...
Route::get('/users/{user}', [UserController::class, 'show']);
 
// Controller method definition...
public function show(User $user)
{
    return view('user.profile', ['user' => $user]);
}
```

## Tags

#Laravel 