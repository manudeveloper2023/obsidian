Además de comprobar el token CSRF como parámetro POST, el middleware `Illuminate\Foundation\Http\Middleware\ValidateCsrfToken` que se incluye en el grupo de middleware web de forma predeterminada, también comprobará el encabezado de solicitud X-CSRF-TOKEN.

```PHP
<meta name="csrf-token" content="{{ csrf_token() }}">
```
## Tags

##### #Laravel
##### #Laravel-CSRF