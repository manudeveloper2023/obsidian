Puedes recuperar el `host` de la solicitud entrante a través de estos métodos

```php
$request->host();
$request->httpHost();
$request->schemeAndHttpHost();

{
    "host": "127.0.0.1",
    "httpHost": "127.0.0.1:8000",
    "schemeAndHttpHost": "http://127.0.0.1:8000"
}
```
## Tags

##### #Laravel
##### #Laravel-Request