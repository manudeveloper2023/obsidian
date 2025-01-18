En caso que quieras crear tus propias directivas , puedes usar el método de `directive`

```php
<?php
 
namespace App\Providers;
 
use Illuminate\Support\Facades\Blade;
use Illuminate\Support\ServiceProvider;
 
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
        Blade::directive('datetime', function (string $expression) {
            return "<?php echo ($expression)->format('m/d/Y H:i'); ?>";
        });
    }
}
```

```php
<!DOCTYPE html>
<html>
<head>
    <title>Directiva @datetime</title>
</head>
<body>
    <h1>Fecha actual</h1>
    <p>La fecha y hora actual es: @datetime($date)</p>
</body>
</html>
```
## Tags

##### #Laravel
##### #Laravel-Blade