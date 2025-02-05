Puedes modificar los mensajes de error del `form request` sobreescribiendo el método de  `messages` 

```php
/**
 * Get the error messages for the defined validation rules.
 *
 * @return array<string, string>
 */
public function messages(): array
{
    return [
        'title.required' => 'A title is required',
        'body.required' => 'A message is required',
    ];
}
```
## Tags

##### #Laravel
##### #Laravel-Validation