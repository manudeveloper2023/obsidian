Para redireccionar puedes usar `Illuminate\Http\RedirectResponse` y contienen los encabezados adecuados necesarios para redirigir al usuario a otra `URL`

```php
Route::get('/dashboard', function () {
    return redirect('/home/dashboard');
});
```

Puede volver a la ubicación anterior , como cuando un formario no es valido , puede usar el método de `back` , que utiliza la sesión del usuario

```php
Route::post('/user/profile', function () {
    // Validate the request...
 
    return back()->withInput();
});
```
## Tags

##### #Laravel
##### #Laravel-Response