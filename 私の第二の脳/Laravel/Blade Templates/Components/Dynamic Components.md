A veces , necesitas poder renderizar un componente pero no sepas qué componente renderizar hasta tiempo de ejecución , en este caso puedes usar un `dynamic-component`

```php
// $componentName = "secondary-button";
 
<x-dynamic-component :component="$componentName" class="mt-4" />
```
## Tags

##### #Laravel