Puedes pasar en los parámetros un **`segundo argumento`** a la función de **`route`**.El ofrece los parametros que automaticamente seran insertados en la **URL** generados en sus respectivas posiciones 

## Ejemplo

```php
Route::get('/user/{id}/profile', function (string $id) {
    // ...
})->name('profile');
 
$url = route('profile', ['id' => 1]);
```

Si pasas parametros adicionales al arreglo , estos seran representados como pares **`llaves y valor`** que se utilizaran como una cadena de querys de **URL**

```php
Route::get('/user/{id}/profile', function (string $id) {
    // ...
})->name('profile');
 
$url = route('profile', ['id' => 1, 'photos' => 'yes']);
 
// /user/1/profile?photos=yes
```
## Tags

##### #Laravel