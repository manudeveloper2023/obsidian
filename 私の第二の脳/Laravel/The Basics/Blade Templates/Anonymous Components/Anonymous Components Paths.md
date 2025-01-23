Es posibles registrarlos desde el método de `services providers` , agregandolos en `boot` y utilizando la función de `anonymousComponentPath` 
## Ejemplo

```php
/**
 * Bootstrap any application services.
 */
public function boot(): void
{
	Blade::anonymousComponentPath(__DIR__.'/../components', 'dashboard');
}
```

```php
<x-dashboard::panel />
```
## Tags

##### #Laravel
##### #Laravel-Blade