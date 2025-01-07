```yaml
services:
  backend:
    image: backend

  db:
    image: mysql

  db-migrations:
    image: backend
    command: myapp migrate
    depends_on:
      - db
    profiles:
      - tools
```

Al ejecutar el **compose** se iniciaran la **db y el backend**

```bash
# Only start backend and db
$ docker compose up -d

# This runs db-migrations (and,if necessary, start db)
# by implicitly enabling the profiles `tools`
$ docker compose run db-migrations
```

Si poseemos un servicio que posea **`depends_on`** debe que tener

El mismo perfil y iniciarse siempre, **`omitiendo perfiles`** o iniciando explícitamente un perfil coincidente

```yaml
services:
  web:
    image: web

  mock-backend:
    image: backend
    profiles: ["dev"]
    depends_on:
      - db

  db:
    image: mysql
    profiles: ["dev"]

  phpmyadmin:
    image: phpmyadmin
    profiles: ["debug"]
    depends_on:
      - db
```

```yaml
# Only start "web"
docker compose up -d

# Start mock-backend (and, if necessary, db)
# by implicitly enabling profiles `dev`
docker compose up -d mock-backend

# This fails because profiles "dev" is not enabled
docker compose up phpmyadmin
```

Se soliciona añadiendo los perfiles necesarios a la base de datos

```bash
db:
  image: mysql
  profiles: ["debug", "dev"]
```

También podria iniciar el perfil de **`dev`** explicitamente

```bash
# Profiles "debug" is started automatically by targeting phpmyadmin
docker compose --profile dev up phpmyadmin
COMPOSE_PROFILES=dev docker compose up phpmyadmin
```
### Tags

###### #Docker