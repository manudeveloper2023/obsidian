
**`/etc/nginx`**

Es el directorio de configuración de **Nginx**.Todos los archivos de configuración de **Nginx** estan aquí

**`/etc/nginx/nginx.conf`**

Archivo de configuración  principal de **Nginx**.Puede ser modificado para realizar cambios en la **`configuración global de Nginx`**

**`/etc/nginx/sites-available/`**

Directorio donde se almacenan los bloques de servidor por sitio.No se **usaran los archivos de configuración** a menos que esten vinculados al directorio de **`sites-enabled`**

**`/etc/nginx/sites-enabled/`**

Donde se almacenan los **`bloques de servidor por sitio habilitados`**.Por lo general , se crean mediante **`vinculos a archivos de configuración`** que se encuentran en el directorio de **`sites-available`**

**`/etc/nginx/snippets`**

Contiene fragmentos de configuración que se pueden incluir en otras partes de la configuración de **Nginx**.Donde se suelen agregar las **`configuraciones más comunes`**

```nginx
# /etc/nginx/snippets/ssl-params.conf 
ssl_protocols TLSv1.2 TLSv1.3; 
ssl_prefer_server_ciphers on; 
ssl_ciphers 'ECDHE-ECDSA-AES256-GCM-SHA384:ECDHE-RSA-AES256-GCM-SHA384'; ssl_session_cache shared:SSL:10m; ssl_session_timeout 10m;
```

Y lo puedes incluir en **`server`**

```Nginx
server {
    listen 443 ssl;
    server_name example.com;

    ssl_certificate /etc/ssl/certs/example.crt;
    ssl_certificate_key /etc/ssl/private/example.key;

    include snippets/ssl-params.conf;
}

```

## Tags

###### #Nginx