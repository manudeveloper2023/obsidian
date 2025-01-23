Al colocar una vista con el `.blade.php` tu aplicación de `resources/views` puedes crearlas usando `make:view`

```bash
php artisan make:view greeting
```

## Ejemplo

```php
use Illuminate\Support\Facades\View;
 
Route::get('/', function () {
    return view('greeting', ['name' => 'James']);
});
// También , se puede retonar como View
return View::make('greeting', ['name' => 'James']);
```
## Tags

##### #Laravel
##### #Laravel-View
