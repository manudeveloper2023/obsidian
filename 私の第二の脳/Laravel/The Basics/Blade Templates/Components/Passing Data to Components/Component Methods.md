Se pueden invocar métodos públicas de los componentes

## Ejemplo

```php
/**
 * Determine if the given option is the currently selected option.
 */
public function isSelected(string $option): bool
{
    return $option === $this->selected;
}
```

Puedes ejecutarlo en el métodoinvocando la variable que coincida con el nombre del método

```php
<option {{ $isSelected($value) ? 'selected' : '' }} value="{{ $value }}">
    {{ $label }}
</option>
```
## Tags

##### #Laravel