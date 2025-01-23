Además de verificar si el archivo está presente , puede verificar que no hubo problemas al cargar el archivo mediante el método de `isValid`

```php
if ($request->file('photo')->isValid()) {
    // ...
}
```
## Tags

##### #Laravel
##### #Laravel-Request