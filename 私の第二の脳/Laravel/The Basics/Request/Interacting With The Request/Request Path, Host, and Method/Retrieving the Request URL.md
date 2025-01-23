Si quieres que te ofrezcan todas la `URL` , puedes usar `url` o `fullUrl` , incluyendo los `query string`

```php
$url = $request->url();
 
$urlWithQueryString = $request->fullUrl();
```

Si quieres agregarles `query parameteres` puedes usar `fullUrlWithQuery`

```php
$request->fullUrlWithQuery(['type' => 'phone']);
```

Para eliminar los `query parameteres` con solo su clave puedes usar

```php
$request->fullUrlWithQuery(['type']);
```
## Tags

##### #Laravel
##### #Laravel-Request