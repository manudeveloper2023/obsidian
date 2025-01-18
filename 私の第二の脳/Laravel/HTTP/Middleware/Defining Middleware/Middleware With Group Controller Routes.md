```php
Route::controller(UserController::class)
    ->middleware(is1Equal1::class)
    ->group(function () {
        Route::get('/user', 'showAll');
        Route::get('/user/{id}', 'show');
        Route::post('/user', 'store');
    })->name('user');
```
## Tags

##### #Laravel