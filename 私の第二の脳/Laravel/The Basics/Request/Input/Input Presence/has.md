Determina si un valor se usa en la `request`.

```php
if ($request->has('name')) {
    // ...
}

if ($request->has(['name', 'email'])) {
    // ...
}
```
## Tags

##### #Laravel
##### #Laravel-Request