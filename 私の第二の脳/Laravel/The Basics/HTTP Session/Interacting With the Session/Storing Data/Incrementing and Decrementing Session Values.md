Si los datos de tu sesión contiene un entero puedes incrementarlos o decrementarlos como un `increment` o `decrement`

```php
$request->session()->increment('count');
 
$request->session()->increment('count', $incrementBy = 2);
 
$request->session()->decrement('count');
 
$request->session()->decrement('count', $decrementBy = 2);
```

## Tags

##### #Laravel
##### #Laravel-Session