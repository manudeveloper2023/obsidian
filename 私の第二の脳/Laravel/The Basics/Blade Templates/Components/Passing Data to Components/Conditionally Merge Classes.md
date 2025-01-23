Si quieres agregar condicionales mediante tus `merge` , puedes crearlos mediante la directiva de `class`

```php
<div {{ $attributes->class(['p-4', 'bg-red' => $hasError]) }}>
    {{ $message }}
</div>
```

Si necesitas agregar otros atributos puedes usar `merge` con `class`

```php
<button {{ $attributes->class(['p-4'])->merge(['type' => 'button']) }}>
    {{ $slot }}
</button>
```