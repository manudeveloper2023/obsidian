
En el caso que quieras utilizar codigo `PHP` en tus vistas , podrias usar la directiva de `@php` 

```php
@php
    $counter = 1;
@endphp
```

También , podrías usar la directiva de `@use` en caso que quieras importar una clase

```php
@use('App\Models\Flight', 'FlightModel')
```
## Tags

##### #Laravel