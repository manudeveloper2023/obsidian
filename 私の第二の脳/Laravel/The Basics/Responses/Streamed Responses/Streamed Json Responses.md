Si necesitas transmitir datos `JSON` de forma incremental , puedes utilizar el método de `streamJson`

```php
use App\Models\User;
 
Route::get('/users.json', function () {
    return response()->streamJson([
        'users' => User::cursor(),
    ]);
});
```

## Tags

##### #Laravel
##### #Laravel-Response