Si necesitas veríficar otros entornos además de producción , puedes usar la directiva de `@env`

```php
@env('local')
    <p>Estás en el entorno local.</p>
@endenv

@env(['staging', 'testing'])
    <p>Estás en el entorno de pruebas.</p>
@endenv
```

## Tags

##### #Laravel