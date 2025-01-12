Se usan para analizar valores de un segmento dinámico

```tsx
<Route path="/concerts/:city" element={<City />} />

import { useParams } from "react-router";

function City() {
  let { city } = useParams();
  let data = useFakeDataLibrary(`/api/v2/cities/${city}`);
  // ...
}
```
## Tags

###### #React 
###### #React-Router 