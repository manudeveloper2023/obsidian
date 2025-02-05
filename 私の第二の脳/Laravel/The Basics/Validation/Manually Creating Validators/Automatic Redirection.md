Si te gustaria crear una validación manual que aproveche la redirección automática que ofrece el método de validación de la solicitud `HTTP` , puede usar `validate` para redirigir automáticamente al usuario o , en el caso de un `XHR` se envie un `JSON`


```PHP
Validator::make($request->all(), [
    'title' => 'required|unique:posts|max:255',
    'body' => 'required',
])->validate();
```

Si quieres usar el `validateWithBag` para almacenar los mensajes de error puedes usar un `named error bag`

```php
Validator::make($request->all(), [
    'title' => 'required|unique:posts|max:255',
    'body' => 'required',
])->validateWithBag('post');
```
## Tags

##### #Laravel
##### #Laravel-Validation