Las vistas separan la lógica de su controlador/aplicación de la lógica de su presentación y se almacenan en el `resources/views`

```php
<!-- View stored in resources/views/greeting.blade.php -->
 
<html>
    <body>
        <h1>Hello, {{ $name }}</h1>
    </body>
</html>
```

Podemos retornar las vistas usando el `helper` de `view`

```php
Route::get('/', function () {
    return view('greeting', ['name' => 'James']);
});
```

## Tags

##### #Laravel
##### #Laravel-View

