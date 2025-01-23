El método `flash` en la clase de `Illuminate\Http\Request` mostrará el `input` actual a la sesión para que esté disponible durante la próxima solicitud del usuario

```php
$request->flash();
```

Puedes usar los métodos de `flashOnly` y `flashExcept` para mostrar un subconjunto de los `request data` de la sesión.

Son útiles para mantener información confidencial

```php
$request->flashOnly(['username', 'email']);
 
$request->flashExcept('password');
```
## Tags

##### #Laravel
##### #Laravel-Request