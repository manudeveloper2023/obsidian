El método de archivo se puede utilizar para mostrar un archivo , como imagen o un PDF , directamente en el navegador del usuario en lugar de iniciar una descarga

Este método acepta la ruta absoluta como primer argumento y una matriz de encabezados como segundo argumento


```php
return response()->file($pathToFile);
 
return response()->file($pathToFile, $headers);
```
## Tags

##### #Laravel
##### #Laravel-Response