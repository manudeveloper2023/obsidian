
Ayudan a ajustar la aplicación de **Compose** para diferentes entornos o casos de uso

## Ejemplo

```yaml
services:
  frontend:
    image: frontend
    profiles: [frontend]

  phpmyadmin:
    image: phpmyadmin
    depends_on: [db]
    profiles: [debug]

  backend:
    image: backend

  db:
    image: mysql
```

Para inicializarlo usaras , para solo utilizar los servicios que posean **debug** o que no tengan ningun perfil asignado

```bash
docker compose --profile debug up
```

```bash
COMPOSE_PROFILES=debug docker compose up
```

Si queremos iniciar muchos perfiles podemos usar

```bash
docker compose --profile frontend --profile debug up
```

```bash
COMPOSE_PROFILES=frontend,debug docker compose up
```

### Tags

###### #Docker




