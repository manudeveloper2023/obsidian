Dado que algunos `frameworks de JavaScript` utilizan atributos prefijados con dos puntos , puedes utilizar el prefijo de `::` que no es una expresión `PHP` 

```php
<x-button ::class="{ danger: isDeleting }">
    Submit
</x-button>
```

`Blade` renderizara este `HTML`

```php
<button :class="{ danger: isDeleting }">
    Submit
</button>
```
## Tags

##### #Laravel