Un `Cross-site request forgeries` son un tipo de `exploit` malicioso mediante el cual se ejecutan `comandos no autorizados` de un usuario autenticado

## Ejemplo


```php
<form action="https://your-application.com/user/email" method="POST">
    <input type="email" value="malicious-email@example.com">
</form>
 
<script>
    document.forms[0].submit();
</script>
```
## Tags

##### #Laravel
##### #Laravel-CSRF
