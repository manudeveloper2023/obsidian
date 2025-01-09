Puede responder automáticamente a las solicitudes **HTTP** las **`opciones de CORS`**.Las cuales son manejadas mediante el middleware de `HandleCors` q se incluye automáticamente en la pila de middleware global de la aplicación

Si quieres configurar los **`CORS`** para la aplicación puedes hacerlo usando el archivo de configuración de cors usando el comando de 

```bash
# Este comando colocara un archivo de configuración cors.php dentro del directorio de configuración de la aplicación
php artisan config:publish cors
```
## Tags

##### #Laravel