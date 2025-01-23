A veces quieres  mostrar elementos en la sesión para la próxima solicitud.Puedes hacerlo mediante el método flash.Después de la siguiente solicitud `HTTP` se eliminara.

Son mensajes de corta duración

```php
$request->session()->flash('status', 'Task was successful!');
```

Si quieres persistir los datos flash para varias solicitud , puedes utilizar el método de `reflash` , que conservará todos los datos `flash` para una solicitud adicional.

Si solo necesitas algunos datos `flash` especificos , puedes utilizar el método de `keep`

```php
$request->session()->reflash();
 
$request->session()->keep(['username', 'email']);
```

Para persistir tus datos `flash` solo para la solicitud actual , puedes usar el método de `now`

```php
$request->session()->now('status', 'Task was successful!');
```
## Tags

##### #Laravel
##### #Laravel-Session