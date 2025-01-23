A veces quieres acceder los datos de un `elemento padre` dentro de un componente.En estos casos puedes usar `@aware` 

```php
<x-menu color="purple">
    <x-menu.item>...</x-menu.item>
    <x-menu.item>...</x-menu.item>
</x-menu>
```

```php
<!-- /resources/views/components/menu/index.blade.php -->
 
@props(['color' => 'gray'])
 
<ul {{ $attributes->merge(['class' => 'bg-'.$color.'-200']) }}>
    {{ $slot }}
</ul>
```

```php
<!-- /resources/views/components/menu/item.blade.php -->
 
@aware(['color' => 'gray'])
 
<li {{ $attributes->merge(['class' => 'text-'.$color.'-800']) }}>
    {{ $slot }}
</li>
```

> La directiva de `@aware` no podra acceder a los datos de los padres si no esta explicitamente pasados por los `HTML attributes`

## Tags

##### #Laravel
##### #Laravel-Blade

