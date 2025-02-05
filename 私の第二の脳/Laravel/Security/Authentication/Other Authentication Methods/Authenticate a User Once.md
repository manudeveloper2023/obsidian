Puedes utilizar el método de `once` para autenticar al usuario para una única solicitud.No se utilizarán sesiones ni cookies

```php
if (Auth::once($credentials)) {
    // ...
}
```
## Tags

##### #Laravel
##### #Laravel-Authentication