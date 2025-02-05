Si tu no quieres usar los `form requests` puedes usar una instancia de `Validator` , para crear tus propias validaciones

```php
<?php
 
namespace App\Http\Controllers;
 
use Illuminate\Http\RedirectResponse;
use Illuminate\Http\Request;
use Illuminate\Support\Facades\Validator;
 
class PostController extends Controller
{
    /**
     * Store a new blog post.
     */
    public function store(Request $request): RedirectResponse
    {
        $validator = Validator::make($request->all(), [
            'title' => 'required|unique:posts|max:255',
            'body' => 'required',
        ]);
 
        if ($validator->fails()) {
            return redirect('/post/create')
                        ->withErrors($validator)
                        ->withInput();
        }
 
        // Retrieve the validated input...
        $validated = $validator->validated();
 
        // Retrieve a portion of the validated input...
        $validated = $validator->safe()->only(['name', 'email']);
        $validated = $validator->safe()->except(['name', 'email']);
 
        // Store the blog post...
 
        return redirect('/posts');
    }
}
```

Si quieres que paren las validacion una vez que una validación individual haya fallado usar `stopOnFirstFailure`

```php
if ($validator->stopOnFirstFailure()->fails()) {
    // ...
}
```
## Tags

##### #Laravel
##### #Laravel-Validation