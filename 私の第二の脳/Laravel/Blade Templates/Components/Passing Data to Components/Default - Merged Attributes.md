A veces puedes que necesites especificar valores predeterminados para los atributos o combinar los valores para lograrlo puedes usar el método de `merge`

```php
<div {{ $attributes->merge(['class' => 'alert alert-'.$type]) }}>
    {{ $message }}
</div>
```

```php
<x-alert type="error" :message="$message" class="mb-4"/>
```

Al final sera renderizado como

```php
<div class="alert alert-error mb-4">
    <!-- Contents of the $message variable -->
</div>
```
## Tags

##### #Laravel