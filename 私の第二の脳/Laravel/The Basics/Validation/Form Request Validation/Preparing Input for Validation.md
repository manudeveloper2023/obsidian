Si necesitas preparar o sanitizar cualquier dato de una `petición` antes de que se apliquen las reglas de validación , puedes usar `prepareForValidation`

```php
use Illuminate\Support\Str;
 
/**
 * Prepare the data for validation.
 */
protected function prepareForValidation(): void
{
    $this->merge([
        'slug' => Str::slug($this->slug),
    ]);
}
```

Si necesitas normalizarlo después de la validación puedes usar `passedValidation`

```php
/**
 * Handle a passed validation attempt.
 */
protected function passedValidation(): void
{
    $this->replace(['name' => 'Taylor']);
}
```
## Tags

##### #Laravel
##### #Laravel-Validation