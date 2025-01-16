Para mostrar un componente , debes que usar el tag de `x-` mediante un `kebab case`

```php
<x-alert/>
<x-user-profile/>
```

Si estan dentro de un directorio como el de `app/View/Components/Inputs/Button.php`  , podemos renderizarlo como

```php
<x-inputs.button/>
```

Si quieres añadir una condicional , puede definirlo mediante `shouldRender` , si retorna `false` no sera renderizado

```php
use Illuminate\Support\Str;
 
/**
 * Whether the component should be rendered
 */
public function shouldRender(): bool
{
    return Str::length($this->message) > 0;
}
```
## Tags

##### #Laravel