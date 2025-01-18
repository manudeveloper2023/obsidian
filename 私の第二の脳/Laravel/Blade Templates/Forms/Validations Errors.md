La directiva de `@error` , te muestra la variable `$message` donde puedes mostrar el mensaje de error

```php
<!-- /resources/views/post/input.blade.php -->
 
<div class="flex flex-col">
    <label for="{{ $name }}">{{ $title }}</label>
    <input name="{{ $name }}" id="{{ $name }}" type="{{ $type }}" value="{{ old($name) }}"
        class="border-b-2 @error($name) is-invalid @enderror" />
    @error($name)
        <div class="alert alert-danger">{{ $message }}</div>
    @enderror
</div>

```

Podemos agregar un `segundo parametro` en caso que la página contenga muchos formularios

```php
<!-- /resources/views/auth.blade.php -->
 
<label for="email">Email address</label>
 
<input
    id="email"
    type="email"
    class="@error('email', 'login') is-invalid @enderror"
/>
 
@error('email', 'login')
    <div class="alert alert-danger">{{ $message }}</div>
@enderror
```
## Tags

##### #Laravel
##### #Laravel-Blade