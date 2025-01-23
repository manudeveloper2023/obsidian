Puedes pasar a los elementos mediante `keys and values` con el método de `with`

## Ejemplo


```php
return view('greeting')
            ->with('name', 'Victoria')
            ->with('occupation', 'Astronaut');
```

```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Greeting</title>
</head>
<body>
    <h1>Hello, {{ $name }}!</h1>
    <p>Your occupation is: {{ $occupation }}</p>
</body>
</html>
```
## Tags

##### #Laravel
##### #Laravel-View
