Cuando envies `JSON requests` a tu aplicación , puedes acceder a los datos de este , mediante el método de `input` siempre que el encabezado de `Content-Type` sea de `application/json`

```php
$name = $request->input('user.name');
```
## Tags

##### #Laravel
##### #Laravel-Request