Se usa para montar volúmenes o mapear directorios entre el sistema y el contenedor.Permite persistir la información

```bash
docker run -v <ruta_en_anfitrión>:<ruta_en_contenedor> <imagen>
```

## Ejemplo

En este caso crearemos una base de datos mediante un contenedor con **postgresql**

```bash
docker run -d \
  --name postgres-container \
  -e POSTGRES_PASSWORD=mysecretpassword \
  -v pgdata:/var/lib/postgresql/data \
  postgres
```
## Tags

###### #Docker

