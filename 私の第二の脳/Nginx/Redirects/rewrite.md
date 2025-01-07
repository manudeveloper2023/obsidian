Modifica la **URl** y sigue procesando la solicitud con la nueva **URL**


## Sintaxis

```nginx
rewrite <patrón> <nueva_url> [<opciones>];
```

## Ejemplo

Si alguien visita `http://example.com/old-category/item1`, Nginx lo redirige automáticamente a `http://example.com/new-category/item1` con un código de redirección 301 (permanente).

```nginx
server {
    listen 80;
    server_name example.com;

    location /old-category/ {
        rewrite ^/old-category/(.*)$ /new-category/$1 permanent;
    }
}
```

## Tags

###### #Nginx
