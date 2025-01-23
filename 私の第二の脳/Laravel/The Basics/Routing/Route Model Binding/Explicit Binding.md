 Si no requieres el uso de una convención implicita basado en el modelo puedes usar explicitamente definiendo las rutas de los modelos en el **`boot`** del **`AppServiceProvider`**

```php
use App\Models\User;
use Illuminate\Support\Facades\Route;
 
/**
 * Bootstrap any application services.
 */
public function boot(): void
{
    Route::model('user', User::class);
}
```

Sucesivamente puedes utilizar el parámetro del usuario 

```php
use App\Models\User;
 
Route::get('/users/{user}', function (User $user) {
    // ...
});
```

En este caso solicitara la ruta con el modelo de usuario con el **ID** de 1 , sucesivamente se generará automáticamente una respuesta **HTTP 404**
## Tags

#Laravel 
