Permite al progamador mandar a navegar al usuario sin que el `interactue` , mayormente se usa para `despues de terminar formularios , cerrar la sesiónpor inactividad , entre otros`.

```tsx
import { useNavigate } from "react-router";

export function LoginPage() {
  let navigate = useNavigate();

  return (
    <>
      <MyHeader />
      <MyLoginForm
        onSuccess={() => {
          navigate("/dashboard");
        }}
      />
      <MyFooter />
    </>
  );
}
```
## Tags

###### #React
###### #React-Router 