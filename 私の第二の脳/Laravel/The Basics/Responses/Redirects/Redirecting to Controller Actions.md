Si quieres genera redirecciones a acciones del controlador.Para ello , pase el nombre del controlador y de la acción al método de acción

```php
use App\Http\Controllers\UserController;
 
return redirect()->action([UserController::class, 'index']);
```

Si tu controlador , requiere parametros , los puedes pasar como segundo parametro

```php
return redirect()->action(
    [UserController::class, 'profile'], ['id' => 1]
);
```
## Tags

##### #Laravel
##### #Laravel-Response