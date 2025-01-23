Hay dos formar principales para interactuar con los datos de la sesión , con el helper de `session` y via una instancia de `Request`

```php
<?php
 
namespace App\Http\Controllers;
 
use Illuminate\Http\Request;
use Illuminate\View\View;
 
class UserController extends Controller
{
    /**
     * Show the profile for the given user.
     */
    public function show(Request $request, string $id): View
    {
        $value = $request->session()->get('key');
 
        // ...
 
        $user = $this->users->find($id);
 
        return view('user.profile', ['user' => $user]);
    }
}
```

Puedes agregar un segundo valor , si no existe sesión se ejecutara este valor

```php
$value = $request->session()->get('key', 'default');
 
$value = $request->session()->get('key', function () {
    return 'default';
});
```
## Tags

##### #Laravel
##### #Laravel-Session

