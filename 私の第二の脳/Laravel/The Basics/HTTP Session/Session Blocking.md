Por defecto , Laravel permite las peticiones de una misma sesión se ejecuten simultáneamente , pero se puede perder los datos de la sesión  que realizan solicitudes simultáneas a  los `endpoints` 


Para solucionar esto , Laravel proporciona una funcionalidad que le permite limitar las solicitudes simultáneas para una sesión determinada

## Ejemplo

El `$lockSeconds` es la cantidad máxima de segundos que debe mantenerse el bloqueo de sesión antes de que se libere

El `$waitSeconds` es la la cantidad de segundos que debe esperar una solicitud mientras intenta obtener un bloqueo de sesión.

Si no agregan ningun argumento , el bloqueo se obtendrá durante un máximo de 10 segundos y las solicitudes esperarán un máximo de 10 segundos


```php
Route::post('/profile', function () {
    // ...
})->block($lockSeconds = 10, $waitSeconds = 10);
 
Route::post('/order', function () {
    // ...
})->block($lockSeconds = 10, $waitSeconds = 10);
```



## Tags

##### #Laravel
##### #Laravel-Session