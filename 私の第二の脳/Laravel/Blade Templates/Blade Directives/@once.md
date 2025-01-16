Se utiliza para asegurarse de que una sección de código (o una vista) solo se ejecute o se incluya una vez durante el ciclo de vida de la página.

```php
@once
    @push('scripts')
        <script>
            // Your custom JavaScript...
        </script>
    @endpush
@endonce
```

También , puedes emplearlas con las directivas de `@push` o `@prepend`

```php
@pushOnce('scripts')
    <script>
        // Your custom JavaScript...
    </script>
@endPushOnce
```
## Tags

##### #Laravel