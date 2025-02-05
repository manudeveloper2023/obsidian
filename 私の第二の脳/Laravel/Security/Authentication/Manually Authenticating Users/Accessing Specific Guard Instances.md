Puedes usar la fachada de `Auth` con el método de `guard` , puedes especificar que `guard` usaras para autenticar el usuario

```php
if (Auth::guard('admin')->attempt($credentials)) {
    // ...
}
```
## Tags

##### #Laravel
##### #Laravel-Authentication