Para recuperar la entrada mostrada en la sesión de la solicitud anterior , invoca el método antiguo en una instancia de `Illuminate\Http\Request`.

El método `old` extraerá los datos de entrada mostrados previamente en la sesión

```php
$title = $request->old('title');
```

También provee un helper global de `old` para mostrar los datos anteriores de la sesión

```php
<input type="text" name="title" value="{{ old('title') }}">
```
## Tags

##### #Laravel
##### #Laravel-Validation