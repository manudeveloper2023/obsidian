Crea un objeto de ubicación personalizado con información útil

## Ejemplo

```tsx
<Route path="/private/user/:id" element={<UserProfile />} />
```

```tsx
import { useNavigate } from "react-router-dom";

function GoToProfile() {
  const navigate = useNavigate();

  const handleClick = () => {
    navigate("/profile/42?referrer=home&theme=dark#info", {
      state: { loggedIn: true }, // Pasamos estado adicional
    });
  };

  return <button onClick={handleClick}>Ir al Perfil del Usuario</button>;
}
```

```tsx
/profile/42?referrer=home&theme=dark#info

Perfil del Usuario
Pathname: /profile/42
ID del usuario (userId): 42
Search (Query String): ?referrer=home&theme=dark
Parámetros de búsqueda:
  - Referrer: home
  - Theme: dark
Hash: #info
State (Estado pasado en la navegación): {"loggedIn":true}
Key: default
```
## Tags

###### #React 
###### #React-Router 