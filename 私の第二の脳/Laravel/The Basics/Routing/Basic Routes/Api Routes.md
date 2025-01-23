Si tu aplicación quieres utilizar **APIs** puedes aplicar el comando de 

```bash
php artisan install:api 
```

```php
Route::get('/user', function (Request $request) {
    return response()->json([
        'name' => 'John Doe',
        'email' => 'jhon@gmail.com'
    ]);
});
```

![[Pasted image 20250106200814.png]]

Puedes cambiar el prefijo de URI de **`/api`** mediante el **`bootstrap/app.php`**

```php
->withRouting(

api: __DIR__.'/../routes/api.php',

apiPrefix: 'api/admin',

// ...

)
```
## Tags

##### #Laravel