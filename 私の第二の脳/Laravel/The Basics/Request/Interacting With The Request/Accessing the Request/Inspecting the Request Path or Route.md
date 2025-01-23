El método de `is` te permite  verificar que `request path` concuerda con un patron otorgado.Puedes usar `*` como una wildcard

```php
if ($request->is('admin/*')) {
    // ...
}
```

Usando `routeIs` , puedes determinar las `peticiones recibidas` que tienen concordancia con `named routes`

```php
if (request()->routeIs('admin.*')) {
    // Esto será true si la ruta activa empieza con "admin."
    echo "Estás en el panel de administración.";
}
```