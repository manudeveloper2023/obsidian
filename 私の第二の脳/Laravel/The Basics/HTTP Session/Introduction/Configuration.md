El archivo de configuración de sesión de una aplicación se almacena en `config/session.php`.Por defecto , se le asigna la `database`

El `session driver` define donde se almacenara los datos de la sesión por cada petición

- `file` - Las sesiones se almacenan en  `storage/framework/sessions`.
- `cookie` - Las sesiones se almacenan en cookies seguras y cifradas.
- `database` - Las sesiones se almacenan en una base de datos relacional.
- `memcached` / `redis` - Las sesiones se almacenan en uno de estos almacenamientos
- `dynamodb` - Las sesiones se almacenan en `AWS DynamoDB`.
- `array` - Las sesiones se almacenan en una `matriz PHP` y no se conservarán.
## Tags

##### #Laravel
##### #Laravel-Session