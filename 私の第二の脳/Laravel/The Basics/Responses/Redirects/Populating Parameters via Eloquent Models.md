Si quieres redireccionar a una ruta con un parámetro `ID` que se está completando a partir de un modelo de `Eloquent` , puede pasar el modelo en sí.El ID se extraerá automáticamente:

```php
// For a route with the following URI: /profile/{id}
 
return redirect()->route('profile', [$user]);
```

Si deseas personalizar el valor que se coloca en el parámetro de ruta , puedes especificar la columna en la definición del parámetro de ruta `(/profile/{id:slug})` o puedes anular el método de `getRouteKey` en su modelo Eloquent

```php
/**
 * Get the value of the model's route key.
 */
public function getRouteKey(): mixed
{
    return $this->slug;
}
```

## Tags

##### #Laravel
##### #Laravel-Response