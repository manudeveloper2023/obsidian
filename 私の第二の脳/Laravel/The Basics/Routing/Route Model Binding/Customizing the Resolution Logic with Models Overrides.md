
Puedes sobreescribir tu modelo con el método de **`resolveRouteBinding`** , el cual recibira el valor del segmento de la **URI**

## Ejemplo

```php
/**
 * Retrieve the model for a bound value.
 *
 * @param  mixed  $value
 * @param  string|null  $field
 * @return \Illuminate\Database\Eloquent\Model|null
 */
public function resolveRouteBinding($value, $field = null)
{
    return $this->where('name', $value)->firstOrFail();
}
```
## Tags

#Laravel 