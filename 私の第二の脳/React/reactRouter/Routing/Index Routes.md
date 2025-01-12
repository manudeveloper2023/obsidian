Se representan en la `<Outlet/>` de su padre en la **URL** del padre 

```tsx
<Routes>
  <Route path="/" element={<Root />}>
    {/* renders into the outlet in <Root> at "/" */}
    <Route index element={<Home />} />

    <Route path="dashboard" element={<Dashboard />}>
      {/* renders into the outlet in <Dashboard> at "/dashboard" */}
      <Route index element={<DashboardHome />} />
      <Route path="settings" element={<Settings />} />
    </Route>
  </Route>
</Routes>
```
## Tags

###### #React 
###### #React-Router 