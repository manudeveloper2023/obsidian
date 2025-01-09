
Por defecto , los **`{{ }}`** viene automaticamente con la funcion de **`htmlspecialchars`** de PHP para evitar ataques de **`XSS`** 

Si los quieres desactivar puedes usar el simbolo de **`!`** , aunque no es muy recomendable


```php
Hello, {!! $name !!}.
```
## Tags

##### #Laravel