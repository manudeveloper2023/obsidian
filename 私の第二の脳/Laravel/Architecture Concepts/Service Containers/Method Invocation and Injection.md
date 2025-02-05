A veces puede que necesites invocar un método de una instancia de objeto y , al mismo tiempo , permitir que el contenedor inyecte las dependencias al método

```php
<?php
 
namespace App;
 
use App\Services\AppleMusic;
 
class PodcastStats
{
    /**
     * Generate a new podcast stats report.
     */
    public function generate(AppleMusic $apple): array
    {
        return [
            // ...
        ];
    }
}
```

Para invocarlo debe usar el método de `call`

```php
use App\PodcastStats;
use Illuminate\Support\Facades\App;
 
$stats = App::call([new PodcastStats, 'generate']);
```

Además , acepta cualquier `PHP callable`

```php
use App\Services\AppleMusic;
use Illuminate\Support\Facades\App;
 
$result = App::call(function (AppleMusic $apple) {
    // ...
});
```
### Tags
##### #Laravel 
##### #Laravel-Service-Containers