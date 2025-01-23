Ejecutará el cierre dado si hay un valor presente en la solicitud y no es una cadena vacía

```php
$request->whenFilled('name', function (string $input) {
    // The "name" value is filled...
}, function () {
    // The "name" value is not filled...
});
```
## Tags

##### #Laravel
##### #Laravel-Request