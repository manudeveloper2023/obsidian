El método de almacenamiento acepta la ruta donde se debe almacenar el archivo en relación con el directorio raíz configurando el sistema de archivos


```php
$path = $request->photo->store('images');

$path = $request->photo->store('images', 's3');
```

Si no desea que se genere automáticamente un nombre de archivo, puede utilizar el método `storeAs`

```php
$path = $request->photo->storeAs('images', 'filename.jpg');
 
$path = $request->photo->storeAs('images', 'filename.jpg', 's3');
```