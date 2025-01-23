Se usa `@include` para permitir incluir una `vista de blade` dentro de otra vista

```php
<div>
    @include('shared.errors' , ['status' => 'complete'])
 
    <form>
        <!-- Form Contents -->
    </form>
</div>
```

Si quieres incluir una vista que puede estar presente o no puedes usar la directiva de `@includeIf` 

```php
@includeIf('view.name', ['status' => 'complete'])
```

Puedes usar `@includeWhen` o `@includeUnless` si quieres renderizarlos o no mediante una `expresion booleana`

```php
@includeWhen($boolean, 'view.name', ['status' => 'complete'])
 
@includeUnless($boolean, 'view.name', ['status' => 'complete'])
```

Y puedes usar `@includeFirst` para marcar la primera vista que existe de una arreglo de vistas

```php
@includeFirst(['custom.admin', 'admin'], ['status' => 'complete'])
```
## Tags

##### #Laravel