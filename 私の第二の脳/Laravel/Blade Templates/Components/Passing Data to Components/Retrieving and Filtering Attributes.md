Puedes filtrar atributos usando el método `filter`

```php
{{ $attributes->filter(fn (string $value, string $key) => $key == 'foo') }}
```

Por conveniencia , puedes usar `whereStartsWith` para recuperar todos los atributos cuyas claves comiencen con la cadena determinada

```php
{{ $attributes->whereStartsWith('wire:model') }}
```

Hay otro , método que los excluye que es `whereDoesntStartWith`

```php
{{ $attributes->whereDoesntStartWith('wire:model') }}
```

Usando el método de `first` , puedes renderizar el primer atributo en la bolsa de `atributos`

```php
{{ $attributes->whereStartsWith('wire:model')->first() }}
```

Si quieres veríficar si un atributo esta presente en el componente , puedes usar el método de `has`

```php
@if ($attributes->has(['name', 'class']))
    <div>All of the attributes are present</div>
@endif
```

Puedes usar `hasAny` para verificar si alguno de los atributos dados está presente en el componente

```php
@if ($attributes->hasAny(['href', ':href', 'v-bind:href']))
    <div>One of the attributes is present</div>
@endif
```

Puedes obtener un `atributo en específico` mediante el método de `get`

```php
{{ $attributes->get('class') }}
```
## Tags

##### #Laravel