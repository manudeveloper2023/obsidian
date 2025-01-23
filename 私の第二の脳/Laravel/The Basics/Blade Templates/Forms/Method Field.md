Debes que añadir la directiva de `@method` para poder realizar `requests` de `PUT` , `PATCH` o `DELETE`

```php
<form action="/foo/bar" method="POST">
    @method('PUT')
 
    ...
</form>
```
## Tags

##### #Laravel
##### #Laravel-Blade