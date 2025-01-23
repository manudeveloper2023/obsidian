Devolverá una matriz que contiene todos los `Content Types` aceptados por la solicitud

```php
$contentTypes = $request->getAcceptableContentTypes();
```

El método `accepts` acepta un arreglo de `Content Types` para ver los que son aceptados por la `request`

```php
if ($request->accepts(['text/html', 'application/json'])) {
    // ...
}
```

Puede usar `prefers` para determinar que tipo  de contenido de una matriz dada de tipos de contenido es el más preferido por la solicitud

```php
$preferred = $request->prefers(['text/html', 'application/json']);
```

Puedes usar `expectsJson()` para veríficar si es de tipo `JSON` de la `request`

```php
if ($request->expectsJson()) {
    // ...
}
```
## Tags

##### #Laravel
##### #Laravel-Request
