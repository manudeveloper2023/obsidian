Puede usarse par aindiciar si a sido seleccionado una opcion que deberia ser `selected`

```php
<select name="version">
    @foreach ($product->versions as $version)
        <option value="{{ $version }}" @selected(old('version') == $version)>
            {{ $version }}
        </option>
    @endforeach
</select>
```
## Tags

##### #Laravel