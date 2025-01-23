Si necesitar controlar el estado y los encabezados de la respuesta , pero también requieres devolver una vista como contenido de la respuestas , puedes usar este método de vista

```php
return response()
            ->view('hello', $data, 200)
            ->header('Content-Type', $type);
```

## Tags

##### #Laravel
##### #Laravel-Response