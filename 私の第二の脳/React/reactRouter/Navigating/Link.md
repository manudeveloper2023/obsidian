Se usa cuando no necesitas estilarlo cuando este `activo`

```tsx
import { Link } from "react-router";

export function LoggedOutMessage() {
  return (
    <p>
      You've been logged out.{" "}
      <Link to="/login">Login again</Link>
    </p>
  );
}
```
## Tags

###### #React
###### #React-Router 