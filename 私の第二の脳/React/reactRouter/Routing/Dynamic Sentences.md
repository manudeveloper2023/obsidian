Si la ruta comienza con `:` se vuelve un `segmento dinámico`.Cuando la ruta coincida con la `URL` , el segmento dinámico se analizará a partir de la `URL` y se proporcionará como parámetro a otras APIs del enrutador como **`useParams`**

## Ejemplo

```tsx
<Route path="teams/:teamId" element={<Team />} />

import { useParams } from "react-router";

export default function Team() {
  let params = useParams();
  // params.teamId
}
```

Puedes tener muchos segmento dinamicos en una sola ruta

```tsx
<Route
  path="/c/:categoryId/p/:productId"
  element={<Product />}
/>

import { useParams } from "react-router";

export default function Team() {
  let { categoryId, productId } = useParams();
  // ...
}
```
## Tags

###### #React 
###### #React-Router 
