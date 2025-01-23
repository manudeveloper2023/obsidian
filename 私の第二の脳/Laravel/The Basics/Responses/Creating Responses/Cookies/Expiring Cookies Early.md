Si quieres remover la cookie haciendola caducar lo puedes usar con `withoutCookie`

```php
return response('Hello World')->withoutCookie('name');
```

Puede usar el método expire del método de facha de `Cookie`

```php
Cookie::expire('name');
```

## Tags

##### #Laravel
##### #Laravel-Response