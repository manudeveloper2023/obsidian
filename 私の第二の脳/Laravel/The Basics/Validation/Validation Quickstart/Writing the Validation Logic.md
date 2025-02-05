Para validar podemos  usar el método de `validate` de `Illuminate\Http\Request`.Si falla la validación aparecera una `Illuminate\Validation\ValidationException` y enviara la respuesta de error al usuario

```php
public function store(Request $request): RedirectResponse
{
    $validated = $request->validate([
        'title' => 'required|unique:posts|max:255',
        'body' => 'required',
    ]);
 
    // The blog post is valid...
    
    return redirect('/posts');
}
```

También puedes usar arreglos para usar las reglas

```php
$validatedData = $request->validate([
    'title' => ['required', 'unique:posts', 'max:255'],
    'body' => ['required'],
]);
```

Asímismo , puedes usar `validateWithBag` para validar la petición y almacenar cualquier mensaje de error dentro de una bolsa de errores

```php
$validatedData = $request->validateWithBag('post', [
    'title' => ['required', 'unique:posts', 'max:255'],
    'body' => ['required'],
]);
```
## Tags

##### #Laravel
##### #Laravel-Validation