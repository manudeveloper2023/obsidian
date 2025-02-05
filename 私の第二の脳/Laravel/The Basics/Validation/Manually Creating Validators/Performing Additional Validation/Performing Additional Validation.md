A veces , es necesario realizar una validación adicional despúes de que se complete la validación inicial mediante `after`

```php
use Illuminate\Support\Facades\Validator;
 
$validator = Validator::make(/* ... */);
 
$validator->after(function ($validator) {
    if ($this->somethingElseIsInvalid()) {
        $validator->errors()->add(
            'field', 'Something is wrong with this field!'
        );
    }
});
 
if ($validator->fails()) {
    // ...
}
```

También , soporta matrices de `__invoke` si su lógica de validación posterior está encapsulada en clases invocables , que recibirán una instancia de `Illuminate\Validation\Validator` con el método `__invoke`


## Tags

##### #Laravel
##### #Laravel-Validation