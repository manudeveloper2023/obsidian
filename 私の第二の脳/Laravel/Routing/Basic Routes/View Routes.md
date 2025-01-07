Si tu ruta necesita retornar una vista , puedes usar **`Route::view`**

```php
Route::view('/welcome', 'welcome');
 
Route::view('/welcome', 'welcome', ['name' => 'Taylor']);
```

## Tags

##### #Laravel
