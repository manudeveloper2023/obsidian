
Si quieres que un **`middleware`** corre durante todo las peticiones **`HTTP`** de la aplicación puedes agregar como una **`global middleware`** en `bootstrap/app.php`

## Ejemplo

Si desea añadir el **`middleware`** al principio de la lista puede usar `preprend`

```php
use App\Http\Middleware\EnsureTokenIsValid;
 
->withMiddleware(function (Middleware $middleware) {
     $middleware->append(EnsureTokenIsValid::class);
})
```
## Tags

##### #Laravel
