
Puedes registrar a un usuario mediante su `PK` , puedes usar `loginUsingId` , la cual acepta la `PK` que quieres autenticar

```php
Auth::loginUsingId(1);
```

También , le puedes pasar el `remember` 

```php
Auth::loginUsingId(1, remember: true);
```
## Tags

##### #Laravel
##### #Laravel-Authentication