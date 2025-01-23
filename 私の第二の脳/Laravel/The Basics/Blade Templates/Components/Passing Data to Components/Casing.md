Los argumentos del constructor del componente deberia usar `camelCase` , mientras que `kebab-case` deberia ser usado para referenciar los nombres de argumentos en tus `HTML attributes`

```php
/**
 * Create the component instance.
 */
public function __construct(
    public string $alertType,
) {}
```

El argumento `$alertType` se puede proporcionar al componente de la siguiente manera:

```php
<x-alert alert-type="danger" />
```
## Tags

##### #Laravel