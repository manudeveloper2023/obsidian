Por defecto , los usuarios no pueden acceder a ningún objeto de los esquemas que no son de su propiedad para permitirlo debes que otorgar el privilegio de `USAGE` en el esquema.Todos tienen privilegios en el `schema` publico

```postgresql
GRANT USAGE ON SCHEMA nombre_esquema TO nombre_usuario;
```

En caso de que quieras crear objetos en un esquema que no es tuyo puedes utilizar el comando de `CREATE`

```postgresql
REVOKE CREATE ON SCHEMA public FROM PUBLIC;
```
## Tags

###### #Postgresql
###### #SQL
