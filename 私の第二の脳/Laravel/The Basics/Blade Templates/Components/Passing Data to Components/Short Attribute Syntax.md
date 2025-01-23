Cuando pases atributos a los componentes , puedes usar la siguiente sintaxis

```php
{{-- Short attribute syntax... --}}
<x-profile :$userId :$name />
 
{{-- Is equivalent to... --}}
<x-profile :user-id="$userId" :name="$name" />
```

## Tags

##### #Laravel