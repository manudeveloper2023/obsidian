Es un método que se ejecuta cuando el valor este presente en el `request`

```php
$request->whenHas('name', function (string $input) {
    // The "name" value is present...
}, function () {
    // The "name" value is not present...
});
```
## Tags

##### #Laravel
##### #Laravel-Request