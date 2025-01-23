Si quieres crear una instancia de `Symfony\Component\HttpFoundation\Cookie` en un método helper de `cookie`  

```php
$cookie = cookie('name', 'value', $minutes);
 
return response('Hello World')->cookie($cookie);
```
## Tags

##### #Laravel
##### #Laravel-Response