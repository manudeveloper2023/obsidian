Para recibir el primer error de las validaciones , puedes usar el método de `first`

```php
$errors = $validator->errors();
 
echo $errors->first('email');
```
## Tags

##### #Laravel
##### #Laravel-Validation
