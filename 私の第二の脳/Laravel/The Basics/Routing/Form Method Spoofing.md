Los formularios de **HTML** no soportan los **`PUT` , `PAT` o `DELETE`**.Por lo que , para definirlos pueden llamarse mediante un método escondido llamado `_method` 

```php
<form action="/example" method="POST">
    <input type="hidden" name="_method" value="PUT">
    <input type="hidden" name="_token" value="{{ csrf_token() }}">
</form>

// Si quiere utilizar el método mediante blade puedes usarlo de esta forma

<form action="/example" method="POST">
    @method('PUT')
    @csrf
</form>
```
## Tags

##### #Laravel