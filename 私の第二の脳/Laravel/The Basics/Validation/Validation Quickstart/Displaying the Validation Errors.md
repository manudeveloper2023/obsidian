Si los campos de solicitud entrantes no pasan las reglas de validación dadas , `Laravel` redirigirá automáticamente al usuario a su ubicación anterior

Además , todos los errores de validación y la entrada de la solicitud se enviarán automáticamente a la `sesión`

Una variable `$errors` se comparte con todas las vistas con el `Illuminate\View\Middleware\ShareErrorsFromSession` que se proporciona por el grupo de middleware `web` 

Esta variable , permite que siempre este una variable `$errors` disponible en las vistas , lo que le permite asumir convenientemente que la variable `$errors` siempre está definida , que se usa mediante al instancía de `Illuminate\Support\MessageBag` 

```php
<!-- /resources/views/post/create.blade.php -->
 
<h1>Create Post</h1>
 
@if ($errors->any())
    <div class="alert alert-danger">
        <ul>
            @foreach ($errors->all() as $error)
                <li>{{ $error }}</li>
            @endforeach
        </ul>
    </div>
@endif
 
<!-- Create Post Form -->
```

## Tags

##### #Laravel
##### #Laravel-Validation