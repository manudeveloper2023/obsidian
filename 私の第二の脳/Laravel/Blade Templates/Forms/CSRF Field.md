Para definir la protección de `@csrf` , puedes agregar una directiva de `blade` para generar el `token field`

```php
<form method="POST" action="/profile">
    @csrf
 
    ...
</form>
```
## Tags

##### #Laravel
##### #Laravel-Blade