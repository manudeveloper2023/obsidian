*Son* una forma de identificar el `**tipo de contenido de un archivo**` que se envia a través de internet

### Estructura de un MIME Type

Un MIME type consta de dos partes separadas por una barra (`/`):

1. **Tipo (Type)**: La categoría general del contenido (por ejemplo, `text`, `image`, `audio`, `application`, etc.).
2. **Subtipo (Subtype)**: El tipo más específico dentro de esa categoría (por ejemplo, `html`, `jpeg`, `json`, etc.).

## Nginx

En **Nginx** los utilizamos un archivo de configuración llamado **`mime.types`** , donde se definen los tipos **MIME** asociados a varias extensiones del archivo 


```nginx
http {
    include       mime.types;
    default_type  application/octet-stream;
    
	# También podemos hacer que Nginx sirva archivos .webp
    types {
        image/webp  webp;
    }
}

```
## Tags

###### #Nginx 
