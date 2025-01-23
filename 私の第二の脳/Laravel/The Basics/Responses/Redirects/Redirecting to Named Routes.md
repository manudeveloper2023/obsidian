Cuando llames al método de `redirect` , con una instancia de `Illuminate\Routing\Redirector` es retornado , que permite  llamar a una ruta con nombre con el método de `route`

```php
return redirect()->route('login');

// For a route with the following URI: /profile/{id}

return redirect()->route('profile', ['id' => 1]);
```
## Tags

##### #Laravel
##### #Laravel-Response