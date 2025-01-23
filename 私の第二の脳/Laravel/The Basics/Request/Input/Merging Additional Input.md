A veces es posible que necesites fusionar manualmente entradas adicionales en los datos de entrada existentes de la solicitud utilizando el método de `merge`

```php
$request->merge(['votes' => 0]);

// Puedes utilizarlo para fusionar entrada en la solicitud si las claves correspondiente aún no existen dentro de los datos de entrada
$request->mergeIfMissing(['votes' => 0]);

// Veríficara si existe votes , si no existe le agrega el 0
```
## Tags

##### #Laravel
##### #Laravel-Request