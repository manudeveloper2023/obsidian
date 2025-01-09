Si desea deshabilitar el `double encoding` , llame al método de **`Blade::withoutDoubleEncoding`** desde el método de arranque

## Ejemplo

```php
<?php
 
namespace App\Providers;
 
use Illuminate\Support\Facades\Blade;
use Illuminate\Support\ServiceProvider;
 
class AppServiceProvider extends ServiceProvider
{
    /**
     * Bootstrap any application services.
     */
    public function boot(): void
    {
        Blade::withoutDoubleEncoding();
    }
}
```
## Tags

##### #Laravel