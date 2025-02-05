Si la solicitud entrante contiene datos anidados , puedes especificarlos mediante un `.`

```php
$request->validate([
    'title' => 'required|unique:posts|max:255',
    'author.name' => 'required',
    'author.description' => 'required',
]);
```

Si tu variable tiene un `.` puedes saltarla usando `\` 

```php
$request->validate([
    'title' => 'required|unique:posts|max:255',
    'v1\.0' => 'required',
]);
```
## Tags

##### #Laravel
##### #Laravel-Validation