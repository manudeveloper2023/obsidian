Para mostrar todas las rutas de nuestra aplicación podemos usar

```bash
php artisan route:list
```

Por defecto no se muestran los **`middlewares`** de las rutas si usas este comando se te mostraran 

```bash
php artisan route:list -v

# Expand middleware groups...

php artisan route:list -vv

# Para esconder cualquier ruta definida por paquetes externos
php artisan route:list --except-vendor

# Rutas definidas por paquetes externos
php artisan route:list --only-vendor
```

