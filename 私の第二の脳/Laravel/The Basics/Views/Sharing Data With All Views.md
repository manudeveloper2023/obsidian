Si quieres pasar datos a todas las vistas , puedes usarlas mediante el método de `share` , usando el `AppServiceProvider` usando `boot` 

```php
<?php
 
namespace App\Providers;
 
use Illuminate\Support\Facades\View;
 
class AppServiceProvider extends ServiceProvider
{
    /**
     * Register any application services.
     */
    public function register(): void
    {
        // ...
    }
 
    /**
     * Bootstrap any application services.
     */
    public function boot(): void
    {
        View::share('key', 'value');
    }
}
```
## Tags

##### #Laravel
##### #Laravel-View
