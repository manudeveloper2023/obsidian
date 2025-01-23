A menudo quieres pasar contenido adicional a tus componentes por via de `$slots`

```php
<!-- /resources/views/components/alert.blade.php -->
 
<div class="alert alert-danger">
    {{ $slot }}
</div>
```

Puedes contener el `$slot` para inyectar contenido dentro del componente

```php
<x-alert>
    <strong>Whoops!</strong> Something went wrong!
</x-alert>
```

A veces un componente requiere renderizar `multiples $slots` diferentes

```php
<!-- /resources/views/components/alert.blade.php -->
 
<span class="alert-title">{{ $title }}</span>
 
<div class="alert alert-danger">
    {{ $slot }}
</div>
```

En este caso , puedes definir el contenido de los `$slot` usando el `x-slot`.Cualquier contenido que no tenga explicitamente el `x-slot` sera pasado en el componente mediante la variable de `$slot`

```php
<x-alert>
    <x-slot:title>
        Server Error
    </x-slot>
 
    <strong>Whoops!</strong> Something went wrong!
</x-alert>
```

Puedes invocar un `$slot` vacio para determinar si el `$slot` contiene contenido

```php
<span class="alert-title">{{ $title }}</span>
 
<div class="alert alert-danger">
    @if ($slot->isEmpty())
        This is default content if the slot is empty.
    @else
        {{ $slot }}
    @endif
</div>
```

Además , se puede utilizar el método de `hasActualContent` para determinar si el espacio contiene algún contenido real que no sea un comentario `HTML`

```php
@if ($slot->hasActualContent())
    The scope has non-comment content.
@endif
```
## Tags

##### #Laravel