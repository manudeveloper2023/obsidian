Si deseas crear tu propia logica de resolución de **binding** de tus modelos , puedes usar **`Route::bind`**.El **closure** que recibira el valor del segmento de **URI** y debe deolver la instancia de la **`clase que se debe inyectar en la ruta`**.

## Ejemplos

En este caso usaremos , el nombre para que la base de datos lo encuentre , en caso contrario que no lo encuentre usara un error **`404`**

```php
use App\Models\User;
use Illuminate\Support\Facades\Route;
 
/**
 * Bootstrap any application services.
 */
public function boot(): void
{
    Route::bind('user', function (string $value) {
        return User::where('name', $value)->firstOrFail();
    });
}
```

En el caso que la ruta este utilizando el **`implicit binding scoping`** , el **`resolveChildRouteBinding`** sera usado para resolver el **`binding`** del hijo del **`modelo padre`**

```php

class Post extends Model
{
    // Relación con los comentarios
    public function comments()
    {
        return $this->hasMany(Comment::class);
    }

    // Método para resolver la vinculación de un comentario dentro de un post
    public function resolveChildRouteBinding($childType, $value, $field)
    {
        // Si el tipo de hijo es 'comment', buscamos el comentario en el contexto de este post
        if ($childType === 'comment') {
            return $this->comments()->where($field, $value)->firstOrFail();
        }

        // Si no es un comentario, utilizamos la implementación predeterminada de la clase padre
        return parent::resolveChildRouteBinding($childType, $value, $field);
    }
}

class Comment extends Model
{
    protected $fillable = ['content'];

    public function post()
    {
        return $this->belongsTo(Post::class);
    }
}

Route::get('/posts/{post}/comments/{comment}', [PostController::class, 'showComment']);

class PostController extends Controller
{
    public function showComment(Post $post, Comment $comment)
    {
        return view('comments.show', [
            'post' => $post,
            'comment' => $comment,
        ]);
    }
}
```

### **¿Cómo funciona esto en la ruta?**

Cuando haces una solicitud como esta:

`GET /posts/1/comments/5`

1. Resuelve el **`Post`** con `id = 1`.
2. Luego, resuelve el **`Comment`** con `id = 5`, pero dentro del contexto del `Post` con `id = 1`.
## Tags

#Laravel 
