Por defecto , incluye el `middleware` de `TrimStrings` y `ConvertEmptyStringsToNull` en la pila de middleware global de su aplicación

Debido a esto, a menudo necesitará marcar sus campos de solicitud `"opcionales"` como `nullable` si no desea que el `null` no sea considerado como `valores nulos`

```php
$request->validate([
    'title' => 'required|unique:posts|max:255',
    'body' => 'required',
    'publish_at' => 'nullable|date',
]);
```
## Tags

##### #Laravel
##### #Laravel-Validation