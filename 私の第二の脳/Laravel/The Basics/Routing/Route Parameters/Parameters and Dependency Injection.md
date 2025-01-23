Si tu ruta tiene dependencias que deseas que el contenedor de servicios de **Laravel** inyecte automáticamente , debes enumerar los parámetros despues de las dependencias

## Ejemplo

```php
use Illuminate\Http\Request;
 
Route::get('/user/{id}', function (Request $request, string $id) {
    return 'User '.$id;
});
```
## Tags

##### #Laravel