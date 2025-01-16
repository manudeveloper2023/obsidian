Sirve para modificar las definiciones de una tabla

## Ejemplo

`Añadir una columna a una tabla`

```postgresql
ALTER TABLE distributors ADD COLUMN address varchar(30);
```

`Añadir una columna con un valor no nulo por defecto`

```postgresql
ALTER TABLE measurements
  ADD COLUMN mtime timestamp with time zone DEFAULT now();
```

`Añadir una columna y rellenarla con un valor diferente del defecto usado anteriormente`

```postgresql
ALTER TABLE transactions
  ADD COLUMN status varchar(30) DEFAULT 'old',
  ALTER COLUMN status SET default 'current';
```

`Eliminar una columna de una tabla`

```postgresql
ALTER TABLE distributors DROP COLUMN address RESTRICT;
```
## Tags

###### #Postgresql
###### #SQL