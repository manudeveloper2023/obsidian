Define un servicio de limite de velocidad personalizable que puedo utilizar para **`restringir la cantidad`** de trafico para un una ruta o un grupo de rutas determinados

## Ejemplo

Establecemos un limite de 60 solicitudes por minuto ,para un identificador de un usuario autenticado y si no lo esta usaremos la dirección **IP** del solicitante

```php
use Illuminate\Cache\RateLimiting\Limit;
use Illuminate\Http\Request;
use Illuminate\Support\Facades\RateLimiter;
 
/**
 * Bootstrap any application services.
 */
protected function boot(): void
{
    RateLimiter::for('api', function (Request $request) {
        return Limit::perMinute(60)->by($request->user()?->id ?: $request->ip());
    });
}
```

Si las solicitudes entrantes superan el límite de velocidad específica , **Laravel** devolverá automáticamente una respuesta con un código de estado **HTTP 429**.Si desea definir su propia respuesta que debe devolverse con un límite de velocidad

```php
RateLimiter::for('global', function (Request $request) {
    return Limit::perMinute(1000)->response(function (Request $request, array $headers) {
        return response('Custom response...', 429, $headers);
    });
});
```

Además , los puedes crear dinamicamente basada en la petición que envie el usuario o su tipo 

```php
RateLimiter::for('uploads', function (Request $request) {
    return $request->user()->vipCustomer()
                ? Limit::none()
                : Limit::perMinute(100);
});
```

## Tags

##### #Laravel