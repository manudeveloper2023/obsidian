Determina el orden de búsqueda de esquema cuando haces una referencia a un objeto como una tabla , vista , entre otros , sin especificar el esquema que pertenece

Para ver los `search path` actuales debes que agregar

```postgresql
SHOW search_path;

 search_path
--------------
 "$user", public
```

En el caso que quieras agregar un `nuevo esquema al search_path` usar

```postgresql
SET search_path TO myschema,public;
```




## Tags

###### #Postgresql
###### #SQL
