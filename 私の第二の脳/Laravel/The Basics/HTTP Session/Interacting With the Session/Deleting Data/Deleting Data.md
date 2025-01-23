Puedes usar `forget` para eliminar un pedazo de datos en la `session`.Si tu quieres remover todos los datos de la sesión  , puedes usar `flush`

```php
// Forget a single key...
$request->session()->forget('name');
 
// Forget multiple keys...
$request->session()->forget(['name', 'status']);
 
$request->session()->flush();
```
## Tags

##### #Laravel
##### #Laravel-Session