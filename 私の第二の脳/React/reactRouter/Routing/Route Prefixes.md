Una `path` sin un elemento prop agrega un prefijo de la ruta a sus `rutas secundarias`

```tsx
<Route path="projects">
  <Route index element={<ProjectsHome />} />
  <Route element={<ProjectsLayout />}>
    <Route path=":pid" element={<Project />} />
    <Route path=":pid/edit" element={<EditProject />} />
  </Route>
</Route>
```
## Tags

###### #React 
###### #React-Router 