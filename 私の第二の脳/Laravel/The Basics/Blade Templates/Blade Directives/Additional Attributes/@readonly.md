Se usa para indicar si un elemento deberia solo leerse

```php
<input
    type="email"
    name="email"
    value="email@laravel.com"
    @readonly($user->isNotAdmin())
/>
```
## Tags

##### #Laravel

