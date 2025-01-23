Para mayor comodidad , los `input values` que contienen fechas yhoras se pueden recuperar como instancia de `Carbon` usando el método de `Date`

```php
$birthday = $request->date('birthday');
```

Como segundo y tercer argumento aceptados por el método fecha se pueden usar para específicar el formato de la fecha y la zona horaria

```php
$elapsed = $request->date('elapsed', '!H:i', 'Europe/Madrid');
```

Si no se presenta un formato valido , se lanzara una `InvalidArgumentException` ;por lo tanto, se recomienda validar la entrada antes de invocar el método de fecha.