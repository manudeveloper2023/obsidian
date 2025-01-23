Para almacenar datos en la sesión , normalmente utilizará el método de `put`

```php
// Via a request instance...
$request->session()->put('key', 'value');
 
// Via the global "session" helper...
session(['key' => 'value']);
```
## Tags

##### #Laravel
##### #Laravel-Session