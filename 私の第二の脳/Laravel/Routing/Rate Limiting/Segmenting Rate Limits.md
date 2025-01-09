A veces quieres segmentar los límites de velocidad por algún valor arbitrario , en estos casos puede usar el método de **`by`** al crear su límite de velocidad

## Ejemplo

```php
RateLimiter::for('uploads', function (Request $request) {
    return $request->user()->vipCustomer()
                ? Limit::none()
                : Limit::perMinute(100)->by($request->ip());
});
```
## Tags

##### #Laravel