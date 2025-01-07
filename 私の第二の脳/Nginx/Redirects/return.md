Se usa para **redirigir o devolver un código de estado HTTP** con una opción de mensaje o **URL específica**

```nginx
return <codigo_de_estado> <URL o texto>;
```

## Ejemplos

```nginx
server {
    listen 80;
    server_name example.com;

    location /old-page {
        return 301 http://example.com/new-page;  # Redirección 301 (permanente)
    }
}
```

```nginx
server {
    listen 80;
    server_name example.com;

    location /old-page {
        return 301 http://example.com/new-page;  # Redirige permanentemente
    }

    location /temporary-page {
        return 302 http://example.com/new-page;  # Redirige temporalmente
    }
}
```

## Tags

###### #Nginx
