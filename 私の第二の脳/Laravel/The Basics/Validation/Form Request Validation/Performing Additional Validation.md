A veces , es necesario una `validación adicional` después de que se complete la `validación inicial`.

Puedes usar el método de `after` debe devolver una matriz de elementos invocables o cierres que se invocarán después de que se complete la validación

```php
use Illuminate\Validation\Validator;
 
/**
 * Get the "after" validation callables for the request.
 */
public function after(): array
{
    return [
        function (Validator $validator) {
            if ($this->somethingElseIsInvalid()) {
                $validator->errors()->add(
                    'field',
                    'Something is wrong with this field!'
                );
            }
        }
    ];
}
```

Como se indicó , la matriz devuelta por el método `after` , también puede contener clases invocables.El método de `__invoke` de estas clases recibirá una instancia de `Illuminate\Validation\Validator`

```php
use App\Validation\ValidateShippingTime;
use App\Validation\ValidateUserStatus;
use Illuminate\Validation\Validator;
 
/**
 * Get the "after" validation callables for the request.
 */
public function after(): array
{
    return [
        new ValidateUserStatus,
        new ValidateShippingTime,
        function (Validator $validator) {
            //
        }
    ];
}
```
## Tags

##### #Laravel
##### #Laravel-Validation