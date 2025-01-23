Puedes usar `withInput` proporcionado por la instancia de `RedirectResponse` para enviar los datos de entrada de la solicitud actual a la sesión antes de redirigir al usuario a una nueva ubicación

Mayormente se hace cuando el usuario posee un error de validación.Una vez que la entrada se envio a la sesión


```php
return back()->withInput();
```

## Tags

##### #Laravel
##### #Laravel-Response