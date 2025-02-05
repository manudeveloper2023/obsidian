Algunos mensajes de error poseen el placeholder de `:value` que se reemplaza con el valor actual del atributo de solicitud.No obstante , talvez requieras customizar estos valores con un representación personalizada

```php
Validator::make($request->all(), [
    'credit_card_number' => 'required_if:payment_type,cc'
]);

// The credit card number field is required when payment type is cc.

// lang/xx/validation.php

'values' => [
    'payment_type' => [
        'cc' => 'credit card'
    ],
],

// The credit card number field is required when payment type is credit card.
```

## Tags

##### #Laravel
##### #Laravel-Validation