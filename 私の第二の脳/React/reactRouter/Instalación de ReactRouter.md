Instalamos mediante **`npm`** 

```bash
npm i react-router
```

Podemos renderizar el **`<BrowserRouter>`** en la aplicación

```tsx
import React from "react";
import ReactDOM from "react-dom/client";
import { BrowserRouter } from "react-router";
import App from "./app";

const root = document.getElementById("root");

ReactDOM.createRoot(root).render(
  <BrowserRouter>
    <App />
  </BrowserRouter>
);
```

## Tags

###### #React 
###### #React-Router 