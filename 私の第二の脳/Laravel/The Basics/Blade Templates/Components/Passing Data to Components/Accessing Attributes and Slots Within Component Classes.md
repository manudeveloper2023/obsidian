Los componentes de `blade` te permiten acceder al nombre del componente, los atributos y la ranura dentro del método de renderización de la clase.

```php
use Closure;
 
/**
 * Get the view / contents that represent the component.
 */
public function render(): Closure
{
    return function () {
        return '<div {{ $attributes }}>Components content</div>';
    };
}
```

El método `render` puede pasar un `$array` como su único argumento.

```php
return function (array $data) {
    // $data['componentName'];
    // $data['attributes'];
    // $data['slot'];
 
    return '<div {{ $attributes }}>Components content</div>';
}
```

> Los elementos de la matriz $data nunca deben incrustarse directamente en la cadena Blade devuelta por su método de renderizado, ya que hacerlo podría permitir la ejecución remota de código a través de contenido de atributos maliciosos.
## Tags

##### #Laravel