Puedes usarlo para devolver una instacia de `Illuminate\Support\ValidatedInput`.Este objeto expone solo , excepto , y todos los métodos para recuperar un `subconjunto de datos validados` o `toda la matriz`

```php
$validated = $request->safe()->only(['name', 'email']);
 
$validated = $request->safe()->except(['name', 'email']);
 
$validated = $request->safe()->all();
```

También , puedes usarlo para iterar sobre este arreglo

```php
// Validated data may be iterated...
foreach ($request->safe() as $key => $value) {
    // ...
}
 
// Validated data may be accessed as an array...
$validated = $request->safe();
 
$email = $validated['email'];
```
## Tags

##### #Laravel
##### #Laravel-Validation