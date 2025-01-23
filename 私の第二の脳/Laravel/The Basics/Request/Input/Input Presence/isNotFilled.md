Si desea determinar si falta un valor en la solicitud o es una cadena vacía, puede utilizarlo

```php
if ($request->isNotFilled(['name', 'email'])) {
    // ...
}
```
## Tags

##### #Laravel
##### #Laravel-Request