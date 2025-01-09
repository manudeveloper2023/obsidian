Permite marcar un campo de tipo checkbox como seleccionado si una condición específica se evalúa como `true`

```php
<form action="/submit" method="POST">
    @csrf
    <label for="subscribe">
        <input type="checkbox" name="subscribe" id="subscribe" @checked(old('subscribe'))>
        Suscribirse al boletín
    </label>
    <button type="submit">Enviar</button>
</form>
```
## Tags

##### #Laravel