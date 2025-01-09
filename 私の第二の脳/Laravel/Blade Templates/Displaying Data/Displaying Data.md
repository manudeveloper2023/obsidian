Si quieres poder mostrar datos a través de tus plantillas de **`Blade`** puedes envolverlas en una variables con `{{ }}` .

## Ejemplo

```php
Route::get('/', function () {
    return view('welcome', ['name' => 'Samantha']);
});
```

Podrías mostrar por ejemplo el nombre

```php
Hello, {{ $name }}.
```
## Tags

##### #Laravel