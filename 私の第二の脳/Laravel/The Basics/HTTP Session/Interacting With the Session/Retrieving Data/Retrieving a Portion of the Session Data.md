Los métodos `only` y `except` se pueden utilizar para recuperar un subconjunto de los datos de la sesión

```php
$data = $request->session()->only(['username', 'email']);
 
$data = $request->session()->except(['username', 'email']);
```
## Tags

##### #Laravel
##### #Laravel-Session