Cuando su aplicación lanza una excepción `Illuminate\Validation\ValidationException` y la solicitud espera una respuesta `JSON` , `Laravel` formateará automáticamente los mensajes de error y devolverá una respuesta `HTTP 422 Unprocessable Entity.`

```php
{
    "message": "The team name must be a string. (and 4 more errors)",
    "errors": {
        "team_name": [
            "The team name must be a string.",
            "The team name must be at least 1 characters."
        ],
        "authorization.role": [
            "The selected authorization.role is invalid."
        ],
        "users.0.email": [
            "The users.0.email field is required."
        ],
        "users.2.email": [
            "The users.2.email must be a valid email address."
        ]
    }
}
```
## Tags

##### #Laravel
##### #Laravel-Validation