Si deseas que el  marcador de posición `:attribute` sea personalizado , puedes especificar los nombres personalizados

```php
/**
 * Get custom attributes for validator errors.
 *
 * @return array<string, string>
 */
public function attributes(): array
{
    return [
        'email' => 'email address',
    ];
}

// Se mostrara como - `The email address is required.`
```
## Tags

##### #Laravel
##### #Laravel-Validation