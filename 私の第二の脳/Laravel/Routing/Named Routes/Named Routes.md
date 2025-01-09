Permiten generar **URL** o **redirecciones** de manera conveniente para rutas específicas

```php
Route::get('/user/profile', function () {
    // ...
})->name('profile');
```

También , los puedes específicar en rutas de controladores

```php
Route::get(
    '/user/profile',
    [UserProfileController::class, 'show']
)->name('profile');
```
## Tags

##### #Laravel