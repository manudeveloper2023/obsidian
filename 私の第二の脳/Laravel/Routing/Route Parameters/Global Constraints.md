Si desea que un parámetro siempre este limitado por una expresión regular determinada , puede usar el **`patern`** en los **`Apps Providers`**

## Ejemplo

```php
use Illuminate\Support\Facades\Route;
 
/**
 * Bootstrap any application services.
 */
public function boot(): void
{
    Route::pattern('id', '[0-9]+');
}
```
## Tags

##### #Laravel