Configuras el **`Dockerfile`** del servicio de backend

```Dockerfile
FROM node:19-alpine  
  
WORKDIR /usr/src/app  
  
COPY package*.json ./  
  
RUN npm install  
  
COPY . .  
  
EXPOSE 5050  
  
CMD [ "node", "index.js" ]
```

Configuramos el **`Dockerfile`** del servicio de **Nginx**

```Dockerfile
FROM nginx:stable-alpine  
  
COPY nginx.conf /etc/nginx/conf.d/default.conf  
  
EXPOSE 80  
  
CMD ["nginx", "-g", "daemon off;"]
```

Configuramos el `default.conf` para la configuración de **`nginx`**

```nginx
upstream backend {
    server backend:5050;    
}

server {
    listen 80;

    resolver 127.0.0.11 valid=5s;
    
    include /etc/nginx/mime.types;

    location / {
        proxy_pass http://backend/;
    }
}
```

Creamos el `docker-compose.yml` para crear nuestros servicios de `backend`

```yml
version: '3'  
services:  
backend:  
build: ../server  
environment:  
- PORT=5050  
deploy:  
replicas: 4  
networks:  
- loadbalancing  
  
nginx:  
build: ../nginx  
container_name: nginx  
ports:  
- "80:80"  
networks:  
- loadbalancing  
depends_on:  
- backend  
  
networks:  
loadbalancing:
```

![[Pasted image 20250106164435.png]]

## Tags

###### #Nginx