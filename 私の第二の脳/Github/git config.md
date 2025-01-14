se utiliza para configurar aspectos del entorno de Git, como información del usuario

```bash
git config user.email
```

### Niveles de configuración 

##### `--local`

Por defecto , `git config` lo configurara en un nivel local si no se pasa ninguna opción de configuración , solo se aplica al repositorio de contexto en el que se invoca.

Se almacenan en un archivo del directorio de `.git` del directorio de `.git/config`

##### `--global`

Es aplicado al sistema operativo del usuario , se almacenan en el directorio del usuario en `~/.gitconfig`

##### `--system`

Se aplica la configuración a toda la maquina , este nivel de configuración cubre a todos los usuarios de un `sistema operativo y todos los repositorios`

### Escribiendo un valor

Puedes escribir un valor mediante la configuración de : 

```bash
git config --global user.email "your_email@example.com"
```
### Algunos usos principales de `git config`:

**Configurar un editor predeterminado:** 

Define el editor de texto que se abrirá cuando sea necesario escribir mensajes de commit, merge, etc.

```bash
git config --global core.editor "code --wait" # Para Visual Studio Code
```


**Mostrar colores en la salida de Git:** 

Hace que las salidas de comandos como `git status` o `git diff` sean más legibles con colores

```bash
git config --global color.ui auto

```

**Alias para comandos:** 

Crea atajos para comandos largos o comunes.

```bash
git config --global alias.st status
git config --global alias.co checkout
```

**Configuración de nivel de línea final (EOL):** 

Ayuda a evitar problemas de conversión de saltos de línea entre sistemas operativos.

```bash
git config --global core.autocrlf true # Para Windows
```

**Configuración de cacheo de credenciales:** 

Guarda tus credenciales para evitar tener que ingresarlas cada vez que interactúas con un repositorio remoto.

```bash
git config --global credential.helper cache
```

**Configuración de ajustes:**

```bash
git config --global --list
```
## Tags

##### #Git

