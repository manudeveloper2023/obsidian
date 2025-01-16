Es una colección de objetos de base de datos dentro de una `PostgreSQL database`.Lo que permite agrupar y aislar de otros objetos de base de datos dentro de otros `schemas`.Su principal objetivo es organizar la base de datos

## Creando un Schema

```bash
CREATE SCHEMA myschema;
```

Para crear o acceder a los objetos dentro de un `schema` , debemos que seguir el patron de 

```postgresql
schema.table

-- Una sintaxis más general podria ser

database.schema.table
```

Puedes eliminarlo mediante el comando de :

```postgresql
DROP SCHEMA myschema;

-- Si quieres eliminar incluyendo todos los elementos dentro usar

DROP SCHEMA myschema CASCADE;
```

Para crear un `schema` para una persona utilizar

```postgresql
CREATE SCHEMA schema_name AUTHORIZATION user_name;
```


## Tags

###### #Postgresql
###### #SQL
