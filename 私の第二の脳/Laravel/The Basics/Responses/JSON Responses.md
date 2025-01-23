Si requieres usar una respuesta con json , este metodo `automaticamente` usa el `Content-Type` con `application/json` , esto convierte un arreglo a `JSON` usando el `json_encode`

```php
return response()->json([
    'name' => 'Abigail',
    'state' => 'CA',
]);
```

Puedes crear un `JSONP` , puedes usar el `json` en una combinación con el `withCallback`

```php
return response()
            ->json(['name' => 'Abigail', 'state' => 'CA'])
            ->withCallback($request->input('callback'));
```
## Tags

##### #Laravel
##### #Laravel-Response