Todas las `cookies` creadas por `Laravel` son encriptadas y firmadas con un `codigo de autenticación` , lo que significa que se considerarán inválidas si han sido modificadas por el cliente.

```php
$value = $request->cookie('name');
```
## Tags

##### #Laravel
##### #Laravel-Request