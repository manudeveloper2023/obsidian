Si quieres parar las validaciones en el  primer error usa `bail`

```php
$request->validate([
    'title' => 'bail|required|unique:posts|max:255',
    // En este caso la regla unique fallo , por lo que max no fue revisado
    
    'body' => 'required',
]);
```
## Tags

##### #Laravel
##### #Laravel-Validation