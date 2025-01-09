Se utilizan para **`enviar metadatos`** o `información adicional` sobre la solicitud o la respuesta

![[Pasted image 20250108180624.png]]

### Entre los headers mas importantes

- **`Authorization`**: Para enviar un token de autenticación.
- **`Accept`**: Para indicar el tipo de contenido que aceptamos.
- **`User-Agent`**: Para identificar el cliente (navegador o aplicación) que está realizando la solicitud.
1. **`Cache-Control`**: Para controlar el almacenamiento en caché.
## Ejemplo

```js
// Función para realizar una solicitud HTTP con encabezados personalizados
const fetchResource = async () => {
  // Definimos la URL del recurso
  const url = 'https://api.ejemplo.com/protected-resource';
  
  // Definimos los encabezados para la solicitud
  const headers = new Headers();
  
  // Agregamos encabezados importantes
  headers.append('Authorization', 'Bearer 123456789abcdef');  // Autenticación con token
  headers.append('Accept', 'application/json');                // Aceptamos solo JSON
  headers.append('User-Agent', 'MyApp/1.0');                   // Identificación del cliente
  headers.append('Cache-Control', 'no-cache');                 // Indicamos que no debe usar caché

  // Realizamos la solicitud con los encabezados
  try {
    const response = await fetch(url, {
      method: 'GET',      // Método de la solicitud (GET)
      headers: headers    // Enviamos los encabezados definidos
    });

    // Verificamos si la respuesta fue exitosa
    if (response.ok) {
      // Parseamos la respuesta JSON
      const data = await response.json();
      console.log('Datos del recurso:', data);
    } else {
      console.log('Error en la solicitud:', response.status);
    }
  } catch (error) {
    console.error('Error en la conexión:', error);
  }
};

// Llamamos a la función para realizar la solicitud
fetchResource();

```
## Tags

##### #HTTP