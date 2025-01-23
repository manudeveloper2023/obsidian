Si tu estas definiendo una ruta que redireccione a otra **URI** , puedes usar **`Route::redirect`** 

```php
Route::redirect('/here', '/there');
```

Por defecto , retorna el codigo de **`302`** , pero puedes utilizar como un estatus que se usa como un tercer parametro

```php
Route::redirect('/here', '/there', 301);
```

O puedes usar **`Route::permanentRedirect`** que retorna en **`301`** code

```php
Route::permanentRedirect('/here', '/there');
```
## Tags

##### #Laravel
