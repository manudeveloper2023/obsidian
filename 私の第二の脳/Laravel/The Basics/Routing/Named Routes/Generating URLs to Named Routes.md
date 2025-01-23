Una vez que asignes los nombre a una ruta , puedes usar el nombre de la ruta cuando generas la **URLs** o redirecciones mediante **`route`** o **`redirects`** 

```php
// Generating URLs...
$url = route('profile');
 
// Generating Redirects...
return redirect()->route('profile');
 
return to_route('profile');
```
## Tags

##### #Laravel