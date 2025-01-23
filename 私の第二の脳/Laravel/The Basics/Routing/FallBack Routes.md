Los puedes usar para definir una ruta que se ejecutara cuando ninguna **`otra coincida con la solicitud entrante`** , normalmente mostraran automáticamente una página **`404`** a través del controlador de excepciones de la aplicación

## Ejemplo

```PHP
Route::fallback(function () {
    return response()->view('errors.404', [], 404);
});
```
## Tags

##### #Laravel