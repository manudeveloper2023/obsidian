**`Post-start`**

Se ejecutaran los comandos antes que el contenedor sea iniciado

## Ejemplo

Una vez que se inicia el contenedor, el comando chown cambia la propiedad del directorio /data al usuario 1001.

```yaml
services:
  app:
    image: backend
    user: 1001
    volumes:
      - data:/data    
    post_start:
      - command: chown -R /data 1001:1001
        user: root

volumes:
  data: {} # a Docker volume is created with root ownership
```

**`Pre-stop`**

Son los comandos que se ejecutan antes de que el contenedor sea **parado**

## Ejemplo

Antes de que el contenedor se detenga , se ejecuta el script **`./data_flush.sh`** para cualquier limpieza necesaria


```yaml
services:
  app:
    image: backend
    pre_stop:
      - command: ./data_flush.sh
```

### Tags

###### #Docker