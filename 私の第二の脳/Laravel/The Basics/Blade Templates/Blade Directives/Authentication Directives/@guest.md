Se usa para verificar si el usuario no está autenticado

```php
@guest
    <!-- Contenido visible solo para usuarios no autenticados -->
@endguest
```

También los puedes usar para roles

```php
@guest('admin')
    <p>Acceso restringido para administradores. Por favor, inicia sesión.</p>
@endguest
```
## Tags

##### #Laravel