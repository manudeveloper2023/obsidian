Cuando escribas componentes a tu propia aplicación , los componentes son descubridos automáticamente dentro del directorio `app/View/Components` y el directorio de `resources/views/components`

Sin embargo , si esta creando un paquete debera registrarlo manualmente la clase del componente y su alias de etiqueta de `HTML`

```php
use Illuminate\Support\Facades\Blade;
 
/**
 * Bootstrap your package's services.
 */
public function boot(): void
{
    Blade::component('package-alert', Alert::class);
}
```

Una vez que este registrado , lo puede renderizar mediante su alias 

```php
<x-package-alert/>
```

Como alternativas , puede utilizar el método `componentNamespace` para cargar automáticamente las clases de componentes por convención

```php
use Illuminate\Support\Facades\Blade;
 
/**
 * Bootstrap your package's services.
 */
public function boot(): void
{
    Blade::componentNamespace('Nightshade\\Views\\Components', 'nightshade');
}
```

Permitira el uso de componentes de paquete por su `namespace` del proveedor

```php
<x-nightshade::calendar />
<x-nightshade::color-picker />
```
## Tags

##### #Laravel