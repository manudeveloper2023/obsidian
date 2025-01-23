Por defecto las rutas de la aplicación son configuradas y cargadas por el **`bootstrap/app.php`**

```php
<?php
 
use Illuminate\Foundation\Application;
 
return Application::configure(basePath: dirname(__DIR__))
    ->withRouting(
        web: __DIR__.'/../routes/web.php',
        commands: __DIR__.'/../routes/console.php',
        health: '/up',
        then: function () {
		    Route::middleware('api')
		        ->prefix('webhooks')
		        ->name('webhooks.')
		        ->group(base_path('routes/webhooks.php'));
		},
    )->create();
```

**`then`** 

Se usa para configurar otras rutas 

`Route::middleware('api')` 

Es el método que se utiliza para aplicar un middleware a un grupo de rutas

`->prefix('webhooks')` 

Agrega un prefijo a todas las rutas definidas dentro de este grupo

En este caso, todas las rutas dentro del archivo `webhooks.php` tendrán el prefijo `/webhooks`. 

Por ejemplo, si una ruta dentro de `webhooks.php` está definida como `Route::get('receive')`, su URL completa será `/webhooks/receive`.

`->name('webhooks.')` 

Asigna un prefijo de nombre a todas las rutas dentro de su grupo

Por ejemplo, si tienes una ruta llamada `receive` dentro de `webhooks.php`, su nombre completo será `webhooks.receive`. 

Esto es útil cuando necesitas hacer referencia a las rutas en otras partes de tu aplicación, como en los redireccionamientos o los enlaces generados mediante la función `route()`.

`->group(base_path('routes/webhooks.php'))`

Agrupa varias rutas bajo un conjunto comun de atributos

Esto significa que todas las rutas dentro de este grupo compartirán las configuraciones definidas (middleware, prefijo y nombre).

`base_path('routes/webhooks.php')`

Carga el archivo de ruats de la aplicación 

Incluso puedes tomar total control de las rutas usando **`using`** closure para el **`withRouting`** method

```php
use Illuminate\Support\Facades\Route;
 
->withRouting(
    commands: __DIR__.'/../routes/console.php',
    using: function () {
        Route::middleware('api')
            ->prefix('api')
            ->group(base_path('routes/api.php'));
 
        Route::middleware('web')
            ->group(base_path('routes/web.php'));
    },
)
```
## Ejemplo

```php
<?php

use Illuminate\Support\Facades\Route;

Route::get('receive', function () {
    return response()->json(['message' => 'Webhook received']);
})->name('receive');

Route::post('notify', function () {
    return response()->json(['message' => 'Webhook received']);
})->name('notify');

```

![[Pasted image 20250106203726.png]]

## Tags

##### #Laravel
