Se utiliza para definir una política de reinicio automático para un contenedor

```BASH
docker run --restart <política> <imagen>
```

## Políticas

**`no`**

Se reiniciará automáticamente cuando se detenga , a menos que sea manualmente

**`always`**

Se reiniciará automáticamente siempre que se detenga, incluso si se detiene de forma normal

**`unless-stopped`**

El contenedor se reiniciará automáticamente si se detiene, a menos que el contenedor sea detenido manualmente por el usuario

**`on-failure[:<número_de_intentos>]`** 

El contenedor se reiniciará solo si termina con un código de error (es decir, un código de salida distinto de 0)

```bash
docker run --restart on-failure:3 <imagen>
```

## Tags

###### #Docker
