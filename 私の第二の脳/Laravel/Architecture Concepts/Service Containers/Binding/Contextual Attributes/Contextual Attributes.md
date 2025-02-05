Puedes usar una variedad de atributos de `contextual binding attributes` que permiten inyectar este tipo de valores sin definir manualmente los enlaces contextuales en los `services providers`

```php
<?php
 
namespace App\Http\Controllers;
 
use Illuminate\Container\Attributes\Storage;
use Illuminate\Contracts\Filesystem\Filesystem;
 
class PhotoController extends Controller
{
    public function __construct(
        #[Storage('local')] protected Filesystem $filesystem
    )
    {
        // ...
    }
}
```

En adición de `Storage`.Laravel ofrece  `Auth`, `Cache`, `Config`, `DB`, `Log`, `RouteParameter`,  y `Tag` como atributos

```php
<?php
 
namespace App\Http\Controllers;
 
use App\Models\Photo;
use Illuminate\Container\Attributes\Auth;
use Illuminate\Container\Attributes\Cache;
use Illuminate\Container\Attributes\Config;
use Illuminate\Container\Attributes\DB;
use Illuminate\Container\Attributes\Log;
use Illuminate\Container\Attributes\RouteParameter;
use Illuminate\Container\Attributes\Tag;
use Illuminate\Contracts\Auth\Guard;
use Illuminate\Contracts\Cache\Repository;
use Illuminate\Database\Connection;
use Psr\Log\LoggerInterface;
 
class PhotoController extends Controller
{
    public function __construct(
        #[Auth('web')] protected Guard $auth,
        #[Cache('redis')] protected Repository $cache,
        #[Config('app.timezone')] protected string $timezone,
        #[DB('mysql')] protected Connection $connection,
        #[Log('daily')] protected LoggerInterface $log,
        #[RouteParameter('photo')] protected Photo $photo,
        #[Tag('reports')] protected iterable $reports,
    )
    {
        // ...
    }
}
```

Además , `Laravel` provee el atributo de `CurrentUser` que inyecta el usuario actualmente autenticado

```php
use App\Models\User;
use Illuminate\Container\Attributes\CurrentUser;
 
Route::get('/user', function (#[CurrentUser] User $user) {
    return $user;
})->middleware('auth');
```

### Tags
##### #Laravel 
##### #Laravel-Service-Containers