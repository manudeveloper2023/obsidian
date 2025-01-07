Sirve para **`redigir`** solicitudes entrantes de un cliente.**Sirve para la configuración** de un **`proxy inverso`**


## Ejemplo

Sirve para que **`Nginx`** actue como intermediario entre el **front** y el **back**

```nginx
location / {
    proxy_pass http://localhost:8080;
}
```

## Tags

###### #Nginx
