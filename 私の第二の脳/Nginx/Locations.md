Permite configurar diferentes comportamientos según la ruta solicitada por el cliente. 

### Usos 

- Redirigir la solicitud a otro servidor (por ejemplo, un servidor backend).

- Servir archivos estáticos (por ejemplo, imágenes, documentos, etc.).

- Aplicar configuraciones específicas para manejar ciertos tipos de solicitudes.

## Ejemplo

```nginx
location / {
    # Configuración para todas las solicitudes a la raíz del servidor
}

location /images/ { # Configuración para solicitudes a '/images/' }

location /api/ { proxy_pass http://localhost:5000; }

location ~ \.(jpg|png)$ { root /data/images; }
```

## Tags

###### #Nginx 
