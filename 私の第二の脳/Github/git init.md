Se usa para inicializar un `nuevo repositorio de Git` en un directorio , creando al directorio de `.git` que contiene toda la información para rastrear los cambios en el proyecto

```bash
cd /path/to/code \ 
git init \ 
git add . \ 
git commit
```

###### `--bare` 

Crea un repositorio desnudo , que no contiene `directorio de trabajo ni archivos del proyecto` , se suele usar como repositorio central para sincronización


![[01.svg]]


###### `--template`

Usan los templates para copiar los archivos necesarios al nuevo repositorio con un predefinido directorio de `.git`

```bash
git init <directory> --template=<template_directory>
```


## Tags

##### #Git
