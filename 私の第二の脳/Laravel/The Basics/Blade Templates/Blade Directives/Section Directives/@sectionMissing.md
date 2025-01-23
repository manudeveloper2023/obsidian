Puedes usarlo para determinar si la sección no esta en el contenido

```php
@sectionMissing('navigation')
    <div class="pull-right">
        @include('default-navigation')
    </div>
@endif
```

## Tags

##### #Laravel