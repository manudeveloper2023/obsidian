Cuando fusiones atributos que no son de `clase` , los valores proporcionados al `merge` seran considerados `default` del atributo.Sin embargo , estos atributos se van a sobreescribir

```php
<button {{ $attributes->merge(['type' => 'button']) }}>
    {{ $slot }}
</button>
```

Al renderizar el componente , con un tipo personalizado , puedes especificarlos cuando consuman el componente.Si el tipo no es especificado , el tipo del boton sera

```php
<x-button type="submit">
Submit
</x-button>
```

Al renderizar el `HTML` el componente del `boton` sera 

```php
<button type="submit">
    Submit
</button>
```

Si desesas que un atributo distinto a class tenga su valor predeterminado y los valores inyectados esten unidos , puedes utilizar el método de `prepend`

```php
<div {{ $attributes->merge(['data-controller' => $attributes->prepends('profile-controller')]) }}>
    {{ $slot }}
</div>
```

Por lo que esto lograra renderizar en `HTML` como

```php
<x-card data-controller="analytics-controller" />
```

```php
<div data-controller="profile-controller analytics-controller">
    <!-- Card content -->
</div>
```
## Tags

##### #Laravel