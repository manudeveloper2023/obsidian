Para determinar si un elemento esta presente en la sesión , puedes usar el método de `has` , que retorna `True` si se presenta 

```php
if ($request->session()->has('users')) {
    // ...
}
```

Si quieres verificarlo aunque su valor sea nulo usar `exists`

```php
if ($request->session()->exists('users')) {
    // ...
}
```

Para determinar que no esta presente en la sesión , puedes usar `missing`

```php
if ($request->session()->missing('users')) {
    // ...
}
```
## Tags

##### #Laravel
##### #Laravel-Session