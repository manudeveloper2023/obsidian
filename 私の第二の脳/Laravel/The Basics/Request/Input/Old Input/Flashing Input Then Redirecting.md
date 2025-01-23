Dado que a menudo quieres actualizar la entrada a la sesión y luego redigirir la página anterior , puedes encadenar fácilmente la entrada `flash` en una redirección usando el método de `withInput`

```php
return redirect('/form')->withInput();
 
return redirect()->route('user.create')->withInput();
 
return redirect('/form')->withInput(
    $request->except('password')
);
```
## Tags

##### #Laravel
##### #Laravel-Request