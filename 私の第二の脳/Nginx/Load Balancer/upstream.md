Define un bloque donde se agrupan las direcciones de los servidores **backend**

```nginx
http {
    upstream backend_servers {
        server backend1.example.com;
        server backend2.example.com;
        server backend3.example.com;
    }

    server {
        listen 80;

        location / {
            proxy_pass http://backend_servers;
        }
    }
}

```
## Tags

###### #Nginx