Puedes considerar los atributos que seran considerados `variables` como `@props`

```php
<!-- /resources/views/components/alert.blade.php -->
 
@props(['type' => 'info', 'message'])
 
<div {{ $attributes->merge(['class' => 'alert alert-'.$type]) }}>
    {{ $message }}
</div>
```


```php
<x-alert type="error" :message="$message" class="mb-4"/>
```
## Tags

##### #Laravel
##### #Laravel-Blade