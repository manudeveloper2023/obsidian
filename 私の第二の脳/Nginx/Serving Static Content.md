Esta configuración se realiza desde el archivo de **`nginx.conf`**

```nginx
http {
        include mime.types;
		listen 80;
		server {
		
		    location / {
		        proxy_pass http://localhost:8080/;
		    }
		
		    location ~ \.(gif|jpg|png)$ {
		        root /data/images;
		    }
		}
}

events { }
```

- **`include mime.types`** : Carga los archivos de tipos **MIME** , que mapean las extensiones de archivos

- **`server`** : Define el servidor virtual , **nginx** puede tener múltiples bloques de **`server`** en un bloque **http**

- **`listen 80`** : Indica que **nginx** escuchara en el puerto 80

- **`root`** : Define la raíz del documento o el directorio donde se encuentran los archivos **estáticos**

- **`location`** : Se utiliza para definir como debe manejar el servidor las solicitudes que coinciden con un **URL**


## Textos relacionados

- ###### **[[Mime Types]]**
- ###### **[[Locations]]**

## Tags

###### #Nginx