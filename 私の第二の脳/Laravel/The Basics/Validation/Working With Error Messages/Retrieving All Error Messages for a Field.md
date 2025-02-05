Si necesitas el arreglo de todos los `mensajes de error de los campos` , puedes usar el método de `get`

```php
foreach ($errors->get('email') as $message) {
    // ...
}
```

Si estas validando un campo de formulario de `arreglo` , puedes recuperar todos los mensajes de `cada uno de los elementos de la matriz` usando el carácter de `*`

```php
foreach ($errors->get('attachments.*') as $message) {
    // ...
}
```
## Tags

##### #Laravel
##### #Laravel-Validation
