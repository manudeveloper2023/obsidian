A veces, puede que necesites transformar una cadena de plantilla de Blade sin formato en HTML válido

```php
use Illuminate\Support\Facades\Blade;
 
return Blade::render('Hello, {{ $name }}', ['name' => 'Julian Bashir']);
```

Las procesa escribiendolas en el directorio de `storage/framework/views` , si quieres que `Laravel` los elimine después de procesarla , puedes usar el `deleteCachedView`

```php
return Blade::render(
    'Hello, {{ $name }}',
    ['name' => 'Julian Bashir'],
    deleteCachedView: true
);
```
## Tags

##### #Laravel
##### #Laravel-Blade