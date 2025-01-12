También conocidos como `catchall` y `start`.Si la ruta termina con el patron con `/*` entonces lo coincidara con `/` incluyendo sus demas caracteres de `/`

```tsx
<Route path="files/*" element={<File />} />

let params = useParams();
// params["*"] will contain the remaining URL after files/
let filePath = params["*"];

// Lo puedes destructurar el * , si lo asignas como un nuevo nombre

let { "*": splat } = useParams();
```
## Tags

###### #React 
###### #React-Router 