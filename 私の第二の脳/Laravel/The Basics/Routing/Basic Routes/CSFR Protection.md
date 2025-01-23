Este es un campo que se utiliza en **`blade`** para evitar los ataques de **CSFR**

```php
<form method="POST" action="/profile">
    @csrf
 
    <!-- Equivalent to... -->
    <input type="hidden" name="_token" value="{{ csrf_token() }}" />
</form>
```
## Tags

##### #Laravel
