Puedes obtener todas las solicitudes entrantes de un cliente usando el método de `all`

```php
$input = $request->all();
```

Puedes usar `collect` para transformar los datos en una `collection`

```php
$request->collect('users')->each(function (string $user) {
    // ...
});
```
## Tags

##### #Laravel
##### #Laravel-Request
