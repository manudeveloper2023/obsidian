Para instalar desde un sistema de **ubuntu** deberemos que utilizar los comandos

```bash
sudo apt update
sudo apt install nginx
```

Antes de testear **Nginx** , testeamos el **firewall** necesario para permitir el acceso al servicio de **Nginx**  , mediante el **`ufw`** 

```bash
sudo ufw app list
```

![[Pasted image 20250105000016.png]]

- **`Nginx Full`**: Abre el puerto **80`(tráfico web normal , sin cifrar)`** como el puerto **443`(tráfico cifrado TLS/SSL)`**. 

- **`Nginx HTTP`**: Habre solo el puerto 80 

- **`Nginx HTTPS`**: Este perfil abre solo el puerto 443 **(tráfico cifrado TLS/SSL)**

Visualizamos el estado del sistema mediante **`systemd`**


```bash
systemctl status nginx
```

![[Pasted image 20250105121140.png]]

Para verificar que esta funcionando correctamente podrías visualizarlo mediante la conexión al la **landing page de Nginx** del localhost en el puerto **`80`**

![[Pasted image 20250105121332.png]]
## Tags

###### #Nginx
