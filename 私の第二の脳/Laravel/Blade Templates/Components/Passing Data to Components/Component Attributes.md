A veces puede que necesites específicar atributos `HTML` adicionales , como las clases , que no son parte de los datos necesarios para que un componente funcione.

```php
<x-alert type="error" :message="$message" class="mt-4"/>
```

Todos los atríbutos que no sean parte del constructor del componente se añadiran en la `bolsa de ataributos` del componente , que se agrega mediante la variable de `$attributes`

```php
<div {{ $attributes }}>
    <!-- Component content -->
</div>
```
## Tags

##### #Laravel