Puedes usar `input` para verificar los valores del `body`

```php
$name = $request->input('name');
```

Puedes pasar un valor por defecto como el segundo argumento del `input` .Este valor sera retornado si el `requested input value` no esta presente en la petición

```php
$name = $request->input('name', 'Sally');
```

Cuando trabajas con formularios que contienen un arreglo de inputs , puedes usar la notación de `.` para acceder a los arreglos

```php
$name = $request->input('products.0.name');
 
$names = $request->input('products.*.name');
```

Puedes llamar el método de `input` sin ningún argumento para recuperar todos los valores de entrada como una matriz asociativa

```php
$input = $request->input();
```
## Tags

##### #Laravel
##### #Laravel-Request