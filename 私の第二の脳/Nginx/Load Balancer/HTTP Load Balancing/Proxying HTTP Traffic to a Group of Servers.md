Mediante la directiva de **`upstream`** podemos definir un grupo de servidores que vamos a utilizar

```nginx
http {
    upstream backend {
        server backend1.example.com weight=5;
        server backend2.example.com;
        server 192.0.0.1 backup;
    }
}
```

Para pasar las peticiones al grupo de servidores , debemos que especificar la directiva de `proxy_pass` 

```nginx
server {
    location / {
        proxy_pass http://backend;
    }
}
```

Al combinar estas dos deberian que ser el **`nginx.conf`** así

```nginx
http {
    upstream backend {
        server backend1.example.com;
        server backend2.example.com;
        server 192.0.0.1 backup;
    }

    server {
        location / {
            proxy_pass http://backend;
        }
    }
}
```

## Tags

###### #Nginx