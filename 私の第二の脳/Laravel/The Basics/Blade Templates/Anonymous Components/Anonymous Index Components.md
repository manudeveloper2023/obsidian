A veces , tu componente esta formado de muchas plantillas de blade , por lo que es posible que quieras agrupar estas plantillas en un solo directorio

## Ejemplo

```php
/resources/views/components/accordion.blade.php
/resources/views/components/accordion/item.blade.php
```

El directorio permitara que puedas renderizar los componentes del acordion y la plantilla se veria como

```php
<x-accordion>
    <x-accordion.item>
        ...
    </x-accordion.item>
</x-accordion>
```
## Tags

##### #Laravel
##### #Laravel-Blade