
```bash
docker compose --profile debug down
```

```bash
COMPOSE_PROFILES=debug docker compose down
```

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
### Tags

###### #Docker