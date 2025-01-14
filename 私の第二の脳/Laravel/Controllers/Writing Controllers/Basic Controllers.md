Sirven para definir la logica de los **`request handling`** estableciendo toda esta lógica en una clase.Por ejemplo , un `userController` , podria `mostrar , actualizar y borrar usuarios`.Son almacenados en el `app/Http/Controllers`

Para crearlos usar

```bash
php artisan make:controller UserController
```

## Ejemplo

Puedo crear esta ruta mediante `show` 

```php
use App\Http\Controllers\UserController;
 
Route::get('/user/{id}', [UserController::class, 'show']);
```

Y despues usando el `controlador` puedo asignar su método

```php
<?php
 
namespace App\Http\Controllers;
 
use App\Models\User;
use Illuminate\View\View;
 
class UserController extends Controller
{
    /**
     * Show the profile for a given user.
     */
    public function show(string $id): View
    {
        return view('user.profile', [
            'user' => User::findOrFail($id)
        ]);
    }
}
```
## Tags

##### #Laravel
##### #Laravel-Controllers