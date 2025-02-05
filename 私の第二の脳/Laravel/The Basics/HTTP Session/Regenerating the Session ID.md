La regeneración del ID de sesión se realiza a menudo para evitar que usuarios malintencionados aprovechen un `session fixation attack` en la aplicación

Laravel regenera automáticamente el `ID` de sesión durante la autenticación si está utilizando los `starter kits` o `Laravel Fortify`

Si lo requiere regenerar manualmente , puede utilizar

```php
$request->session()->regenerate();
```

Si quieres regenerar el sesión `ID` y remover todos los datos en la sesión , puede usar `invalidate`

```php
$request->session()->invalidate();
```
## Tags

##### #Laravel
##### #Laravel-Session