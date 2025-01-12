Son los valores despues de `?` en la **`URL`**.Son accesibles a travez de `useSearchParams` , que retorna una instancia de `URLSearchParams`

```tsx
function SearchResults() {
  let [searchParams] = useSearchParams();
  return (
    <div>
      <p>
        You searched for <i>{searchParams.get("q")}</i>
      </p>
      <FakeSearchResults />
    </div>
  );
}
```
## Tags

###### #React 
###### #React-Router 