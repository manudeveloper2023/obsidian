Proporciona una forma conveniente de inyectar automáticamente las instancias de modelo directamente en sus rutas

## Ejemplo

Buscara el identificador del usuario usando el metodo de **`User::find(id)`** , lo cual lo inyectara en el parámetro **`$user`** si es que existe

```php
use App\Models\User;
 
Route::get('/users/{user}', function (User $user) {
    return $user->email;
});
```

## Tags

##### #Laravel