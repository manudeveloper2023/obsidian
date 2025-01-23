Al redireccionar una `URL` y mostrar datos de la sesión son usualmente usados al mismo tiempo.Normalmente , esto se hace cuando posees un mensaje de éxito a la sesión

```php
Route::post('/user/profile', function () {
    // ...
 
    return redirect('/dashboard')
		   ->with('status', 'Profile updated!');
});
```

Despues , de ser redireccionado , puedes mostrar los mensajes de la sesión

```php
@if (session('status'))
    <div class="alert alert-success">
        {{ session('status') }}
    </div>
@endif
```
## Tags

##### #Laravel
##### #Laravel-Response