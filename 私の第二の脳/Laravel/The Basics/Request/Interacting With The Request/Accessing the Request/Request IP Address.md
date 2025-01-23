Usando el método de `ip` te dara la dirección ip del cleinte que realiza un `request` a la aplicación

```php
$ipAddress = $request->ip();
```

Si quieres obtener un `array` de `IPs` , seran incluidas hasta las direcciones IP de clientes que fueron reenviadas por servidores proxy

```php
$ipAddresses = $request->ips();
```
## Tags

##### #Laravel
##### #Laravel-Request