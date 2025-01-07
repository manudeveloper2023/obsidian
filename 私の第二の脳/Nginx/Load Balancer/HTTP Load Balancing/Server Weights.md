
Distribuye las solicitudes entre los servidores de grupo según sus pesos usando **`Round Robbin`**

## Ejemplo

De cada 6 solicitudes , 5 se envian a **`backend1`** y 1 llega a **`backend2`**
```nginx
upstream backend {
    server backend1.example.com weight=5;
    server backend2.example.com;
    server 192.0.0.1 backup;
}
```

## Tags

###### #Nginx