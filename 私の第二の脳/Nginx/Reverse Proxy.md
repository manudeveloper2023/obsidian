Es un servidor intermediario que se encuentra entre los clientes y uno o más servidores backend

Se encarga de recibir **solicitudes de los clientes** y procesarlas y reenviarlas al servidor backend adecuado 

![[Pasted image 20250104235303.png]]


Supongamos que tienes un sitio web con dos componentes principales:

- Una API backend corriendo en `http://api.example.com:8080`
- Una interfaz web en `http://frontend.example.com:3000`

Con un reverse proxy configurado **(como Nginx o Apache)**, podrías exponer todo en un solo dominio (como `example.com`):

- `https://example.com/api` redirige las solicitudes a `http://api.example.com:8080`.
- `https://example.com/` sirve la interfaz desde `http://frontend.example.com:3000`.

## Tags

###### #Nginx