El método de `download` puede ser usado para generar una respuesta que obligue al navegador del usuario a descargar el archivo en la ruta indicada

Acepta un segundo argumento del método , que determinará el nombre de archivo que verá el usuario al descargar el archivo.

Por último , puede pasar una matriz de encabezados HTTP como tercer argumento

```php
return response()->download($pathToFile);
 
return response()->download($pathToFile, $name, $headers);
```
## Tags

##### #Laravel
##### #Laravel-Response