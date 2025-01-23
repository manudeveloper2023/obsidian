Si necesitas , poder retornar un arreglo de limite con una configuración de limitador de velocidad determinada.

Cada **`límite de velocidad`** se evaluará para la ruta en función del orden en que se coloquen dentro de la matriz

## Ejemplo

```php
RateLimiter::for('login', function (Request $request) {
    return [
        Limit::perMinute(500),
        Limit::perMinute(3)->by($request->input('email')),
    ];
});
```

Si quieres asignar múltiples límites de acceso puedes usar el `by` para segmentarlos

```php
RateLimiter::for('uploads', function (Request $request) {
    return [
        Limit::perMinute(10)->by('minute:'.$request->user()->id),
        Limit::perDay(1000)->by('day:'.$request->user()->id),
    ];
});
```
