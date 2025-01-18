Te permite enviar archivos a pilas con nombres que se pueden representar en otro lugar de otra vista o diseño.Esto puede resultar particularmente útil para especificar las bibliotecas de JavaScript que requieren las vistas secundarias
## Ejemplo

Puedes usar `@push` o `@prepend` para agregarlos al `stack`

```php
@push('scripts')
    This will be second...
@endpush
 
// Later...
 
@prepend('scripts')
    This will be first...
@endprepend
```

Tu puedes agregar un booleano en caso que quieras evaluarlo con `@pushIf`

```php
@pushIf($shouldPush, 'scripts')
    <script src="/example.js"></script>
@endPushIf
```

Puedes mostrar el contenido completo de la pila , con la directiva de `@stack`

```php
<head>
    <!-- Head Contents -->
 
    @stack('scripts')
</head>
```
## Tags

##### #Laravel
##### #Laravel-Blade