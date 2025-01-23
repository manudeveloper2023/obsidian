Tener en cuenta que la mayoría de los métodos de respuesta se pueden encadenar, lo que permite la construcción fluida de instancias de respuesta

```php
return response($content)
            ->header('Content-Type', $type)
            ->header('X-Header-One', 'Header Value')
            ->header('X-Header-Two', 'Header Value');

// También puedes usar withHeaders

return response($content)
            ->withHeaders([
                'Content-Type' => $type,
                'X-Header-One' => 'Header Value',
                'X-Header-Two' => 'Header Value',
            ]);
```
## Tags

##### #Laravel
##### #Laravel-Response