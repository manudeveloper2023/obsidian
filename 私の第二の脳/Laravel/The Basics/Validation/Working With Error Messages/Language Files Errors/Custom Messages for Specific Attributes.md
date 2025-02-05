Para customizar los `mensajes de error` pueden ser especificados con una combinación de `atributos y reglas` dentro de tu aplicación , puedes añadirlas en `lang/xx/validation.php`

```php
'custom' => [
    'email' => [
        'required' => 'We need to know your email address!',
        'max' => 'Your email address is too long!'
    ],
],
```
## Tags

##### #Laravel
##### #Laravel-Validation