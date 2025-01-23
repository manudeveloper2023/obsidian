Mientras el método de  `input` recupera los valores de los `query strings` del request

```php
$name = $request->query('name');
```

Si no hay datos presente , el segundo argumento del método  es retornado como el valor por defecto

```php
$name = $request->query('name', 'Helen');
```

Puedes llamar el método de consulta sin ningún argumento para recuperar todos los valores de la cadena de consulta

```php
$query = $request->query();
```
## Tags

##### #Laravel
##### #Laravel-Request