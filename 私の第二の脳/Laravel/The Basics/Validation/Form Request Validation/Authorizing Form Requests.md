El `Form Request Class` también tiene un `authorize` , dentro puedes determinar si el usuario lo puede realizar

```php
use App\Models\Comment;
 
/**
 * Determine if the user is authorized to make this request.
 */
public function authorize(): bool
{
    $comment = Comment::find($this->route('comment'));
 
    return $comment && $this->user()->can('update', $comment);
}
```

El método de `$this->route('comment')` te otorga los paramétros de la `ruta`

```php
Route::post('/comment/{comment}');
```

Si la ruta te retorna falso , devolvera un `HTTP Response 403`
## Tags

##### #Laravel
##### #Laravel-Validation