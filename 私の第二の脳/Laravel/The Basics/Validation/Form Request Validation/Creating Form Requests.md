Para escenarios de validación más complejos , es posible que se desee crear una `solicitud de formulario` son clases de solicitud personalizadas que `encapsulan la logica de validación y autorización`

Para crearlos se usa `artisan`

```bash
php artisan make:request StorePostRequest
```

Aparecera en `app/Http/Request` y tendra dos métodos de `authorize` y `rules`

```php
/**
 * Store a new blog post.
 */
public function store(StorePostRequest $request): RedirectResponse
{
    // The incoming request is valid...
 
    // Retrieve the validated input data...
    $validated = $request->validated();
 
    // Retrieve a portion of the validated input data...
    $validated = $request->safe()->only(['name', 'email']);
    $validated = $request->safe()->except(['name', 'email']);
 
    // Store the blog post...
 
    return redirect('/posts');
}
```

Si falla esta validación , se redireccionara a la ubicación anterior , los erroes también se mostaran en la sesión para que estén disponibles para la visualización.

Si esta fue una solicitud `XHR` , se devolverá al usuario una respuesta HTTP con un código de estado `422` que incluye una representación `JSON` de los errores de validación.
## Tags

##### #Laravel
##### #Laravel-Validation