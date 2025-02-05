`Laravel` nos permite vincular una interfaz a una implementación determinada.

```php
use App\Contracts\EventPusher;
use App\Services\RedisEventPusher;
 
$this->app->bind(EventPusher::class, RedisEventPusher::class);
```

Esto indica que debe inyectar un `RedisEventPusher` cuando una clase requiera una implementación de `EventPusher`

```php
use App\Contracts\EventPusher;
 
/**
 * Create a new class instance.
 */
public function __construct(
    protected EventPusher $pusher,
) {}
```
### Tags
##### #Laravel 
##### #Laravel-Service-Containers