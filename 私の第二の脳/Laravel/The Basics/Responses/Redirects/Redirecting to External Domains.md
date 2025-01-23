A veces requieres redireccionar a un dominio afuera de mi aplicación.Si llamas al método de `away` , que crea una `RedirectResponse` sin codificación, validación ni verificación de URL adicionales:

```php
return redirect()->away('https://www.google.com');
```
## Tags

##### #Laravel
##### #Laravel-Response