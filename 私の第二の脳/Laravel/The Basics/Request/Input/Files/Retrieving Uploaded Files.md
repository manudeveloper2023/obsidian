Puede recuperar archivos cargados desde una `request` usando el método de archivo o usando propiedades dinámicas.El método de archivo devuelve una instancia de `Illuminate\Http\UploadedFile` , que extiene la clase `PHP SplFileInfo` y proporciona una variedad de métodos para interactuar el archivo

```php
$file = $request->file('photo');
 
$file = $request->photo;
```

Puedes determinar si es un archivo usando el `hasFile`

```php
if ($request->hasFile('photo')) {
    // ...
}
```
## Tags

##### #Laravel
##### #Laravel-Request