Si quieres pasar datos pasando los atributos de `HTML` , si quieres pasar variables mediante `PHP` deben que utilizar el carácter de `:` como prefijo

```php
<x-alert type="error" :message="$message"/>
```

Puedes definir todos los componentes en el constructor de la clase.Todas las propiedades  públicas puede utilizar la vista del componente 

```php
class Alert extends Component
{
    /**
     * Create the component instance.
     */
    public function __construct(
        public string $type,
        public string $message,
    ) {}
 
    /**
     * Get the view / contents that represent the component.
     */
    public function render(): View
    {
        return view('components.alert');
    }
}
```

Cuando tu componente este renderizado , puedes mostrar el contenido de tus variables publicas del componente 

```php
<div class="alert alert-{{ $type }}">
    {{ $message }}
</div>
```
## Tags

##### #Laravel