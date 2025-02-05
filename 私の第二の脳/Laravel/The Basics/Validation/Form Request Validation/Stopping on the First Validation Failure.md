Al agregar una propiedad de `stopOnFirstFailure` a su clase de solicitud , puede informar al `Validator` que debe dejar de validar todos los atributos una vez que se hayan producido una falla

```php
/**
 * Indicates if the validator should stop on the first rule failure.
 *
 * @var bool
 */
protected $stopOnFirstFailure = true;
```

## Tags

##### #Laravel
##### #Laravel-Validation