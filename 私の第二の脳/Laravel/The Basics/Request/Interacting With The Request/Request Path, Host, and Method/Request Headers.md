Si quieres obtener los encabezados de la `Request` puedes usar los métodos de los encabezados.Si no hay encabezados en la `request `aparecera `null`


```php
$value = $request->header('X-Header-Name');
 
$value = $request->header('X-Header-Name', 'default');
```

Puedes usar `hasHeader` para usarlo para determinar si este `request` contiene un header

```php
if ($request->hasHeader('X-Header-Name')) {
    // ...
}
```

En el caso que estes usando un `bearerToken` puede ser usados para recuperar un `bearer token` de un `Authorization`.

```php
$token = $request->bearerToken();
```
## Tags

##### #Laravel
##### #Laravel-Request