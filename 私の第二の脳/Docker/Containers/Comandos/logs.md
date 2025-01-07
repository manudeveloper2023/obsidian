Se usan para proporcionar la información sobre lo que esta pasando en un contenedor 

## Ejemplo

```bash
docker run --name mi_contenedor -d ubuntu

# Obtener sus logs
docker logs mi_contenedor

# Visualizarlos a tiempo real
docker logs -f mi_contenedor

# Mirar los últimos 50 registros
docker logs --tail 50 mi_contenedor
```

## Tags

###### #Docker
