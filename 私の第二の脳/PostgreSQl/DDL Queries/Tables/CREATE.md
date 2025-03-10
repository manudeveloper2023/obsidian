Creando una tabla de `films` y `distributors`

```postgresql
CREATE TABLE films (
    code        char(5) CONSTRAINT firstkey PRIMARY KEY,
    title       varchar(40) NOT NULL,
    did         integer NOT NULL,
    date_prod   date,
    kind        varchar(10),
    len         interval hour to minute
);

CREATE TABLE distributors (
     did    integer PRIMARY KEY GENERATED BY DEFAULT AS IDENTITY,
     name   varchar(40) NOT NULL CHECK (name <> '')
);
```

```postgresql
CREATE TABLE films (
    code        char(5),
    title       varchar(40),
    did         integer,
    date_prod   date,
    kind        varchar(10),
    len         interval hour to minute,
    CONSTRAINT production UNIQUE(date_prod)
);
```

`Creación de verificación en las tablas`

```postgresql
CREATE TABLE distributors (
    did     integer,
    name    varchar(40),
    CONSTRAINT con1 CHECK (did > 100 AND name <> '')
);
```

`Creación de llave primaria compuesta`

```postgresql
CREATE TABLE films (
    code        char(5),
    title       varchar(40),
    did         integer,
    date_prod   date,
    kind        varchar(10),
    len         interval hour to minute,
    CONSTRAINT code_title PRIMARY KEY(code,title)
);
```

`Definiendo una restricción de llave primaria`

Los dos ejemplos son los mismos

```postgresql
CREATE TABLE distributors (
    did     integer,
    name    varchar(40),
    PRIMARY KEY(did)
);

CREATE TABLE distributors (
    did     integer PRIMARY KEY,
    name    varchar(40)
);
```

`Generar valores por defecto`

```postgresql
CREATE TABLE distributors (
    name      varchar(40) DEFAULT 'Luso Films',
    did       integer DEFAULT nextval('distributors_serial'), -- Columna 'did' de tipo integer, cuyo valor por defecto es el siguiente valor de una secuencia 
    modtime   timestamp DEFAULT current_timestamp
);
```

`Creando una tabla especificando un factor de relleno`

Se usa para optimizar el almacenamiento de la tabla y los índices relacionados.

```postgresql
CREATE TABLE distributors (
    did     integer,
    name    varchar(40),
    UNIQUE(name) WITH (fillfactor=70)
)
WITH (fillfactor=70);
```

`Creación de tabla para evitar que dos circulos se sobrepongan`

```postgresql
CREATE TABLE circles (
    c circle, 
    EXCLUDE USING gist (c WITH &&) -- Restricción EXCLUDE con índice GiST
);
```

`Creando una tabla compuesta y una tabla tipada`

```postgresql
CREATE TYPE employee_type AS (name text, salary numeric);

CREATE TABLE employees OF employee_type (
    PRIMARY KEY (name),
    salary WITH OPTIONS DEFAULT 1000
);
```

## Tags

###### #Postgresql
###### #SQL