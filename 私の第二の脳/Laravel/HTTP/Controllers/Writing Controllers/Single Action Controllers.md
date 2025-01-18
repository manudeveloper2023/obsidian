Si una acción de un controlador es particularmente compleja , podrias buscar conveniente dedicar una `clase de controlador entera` en una simple acción.

## Ejemplo

Puedes invocarlo mediante el metodo de `--invokable`

```bash
php artisan make:controller ProvisionServer --invokable
```

Puedes registrar las rutas , a los controladores que solo realicen sola acción

```php
use App\Http\Controllers\ProvisionServer;
 
Route::post('/server', ProvisionServer::class);
```

```php
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

class ProvisionServer extends Controller
{
    /**
     * Provision a new web server.
     */
    public function __invoke(Request $request)
    {
        // Aquí podrías poner la lógica para aprovisionar el servidor
        // Como ejemplo, simplemente vamos a devolver un mensaje
        return response()->json(['message' => 'Server provisioned successfully!']);
    }
}
```
## Tags

##### #Laravel
##### #Laravel-Controllers