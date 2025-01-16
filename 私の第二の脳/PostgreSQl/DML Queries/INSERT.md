`Inserción de datos mediante una subconsulta`

```postgresql
WITH upd AS (
  UPDATE employees SET sales_count = sales_count + 1 WHERE id =
    (SELECT sales_person FROM accounts WHERE name = 'Acme Corporation')
    RETURNING *
)

INSERT INTO employees_log SELECT *, current_timestamp FROM upd;
```

`Manejador de errores en las inserciones`

```postgresql
INSERT INTO distributors (did, dname)
    VALUES (5, 'Gizmo Transglobal'), (6, 'Associated Computing, Inc')
    ON CONFLICT (did) DO UPDATE SET dname = EXCLUDED.dname;
```


## Tags

###### #Postgresql
###### #SQL