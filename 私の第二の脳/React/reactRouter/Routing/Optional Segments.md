Tu puedes crear un segmento opcional añadiendo `?` al final del segmento

## Ejemplo

```tsx
<Route path=":lang?/categories" element={<Categories />} />

// También puedes añadir mas de uno

<Route path="users/:userId/edit?" component={<User />} />
```
## Tags

###### #React 
###### #React-Router 