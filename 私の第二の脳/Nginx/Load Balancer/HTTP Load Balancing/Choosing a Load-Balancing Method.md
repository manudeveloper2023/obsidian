
**`Round Robin`**

Las peticiones se distribuyen de manera uniforme entre todos los servidores y se tiene en cuenta **los pesos de los servidores**.Es **`usado por defecto`**

```nginx
upstream backend {
   # no load balancing method is specified for Round Robin
   server backend1.example.com;
   server backend2.example.com;
}
```

**`Least Connections`**

Se envia la solicitud al servidor con la menor cantidad de conexiones activas

```nginx
upstream backend {
    least_conn;
    server backend1.example.com;
    server backend2.example.com;
}
```

**`IP Hash`**

El servidor se determina a partir de la dirección IP del cliente.Que sera enviado **siempre** al mismo servidor asegurando que el estado de su sesión se mantenga

```nginx
upstream backend {
    ip_hash;
    server backend1.example.com;
    server backend2.example.com;
}
```

Si necesitas **`eliminar temporalmente un servidor`** del balanceador de carga , se puede marcar con `down` 

```nginx
upstream backend {
    server backend1.example.com;
    server backend2.example.com;
    server backend3.example.com down;
}
```

**`Generic Hash`**

El servidor al que se envía una solicitud se determina a partir de una clave definida por el usuario

```nginx
upstream backend {
    hash $request_uri consistent;
    server backend1.example.com;
    server backend2.example.com;
}
```

**`Least Time`**

Para cada solicitud, NGINX Plus selecciona el servidor con la latencia promedio más baja y la menor cantidad de conexiones activas

```nginx
upstream backend {
    least_time header;
    server backend1.example.com;
    server backend2.example.com;
}
```

**`Random`**

Cada solicitud se enviará a un servidor seleccionado aleatoriamente. Si se especifica el parámetro two, primero, NGINX selecciona aleatoriamente dos servidores teniendo en cuenta el peso de los servidores

- **`less_conn`** 
La menor cantidad de conexiones activas

- **`least_time=header (NGINX Plus)`** 
El menor tiempo promedio para recibir el encabezado de respuesta del servidor ($upstream_header_time)1 

- **`least_time=last_byte (NGINX Plus)`** 
El menor tiempo promedio para recibir la respuesta completa del servidor ($upstream_response_time)


```nginx
upstream backend {
    random two least_time=last_byte;
    server backend1.example.com;
    server backend2.example.com;
    server backend3.example.com;
    server backend4.example.com;
}
```

## Tags

###### #Nginx