Es un componente si necesitas estilar el estado activo

```tsx
export const Dashboard = () => {
	return (
		<>
			<nav className="py-6  shadow-md flex justify-center space-x-20">
				<NavLink
					to="/private/home"
					className={({ isActive }) =>
						isActive ? 'text-red-500' : 'text-black'
					}
					end
				>
					Home
				</NavLink>
				<NavLink
					to="/private/about"
					className={({ isActive }) =>
						isActive ? 'text-red-500' : 'text-black'
					}
					end
				>
					About
				</NavLink>
				<NavLink
					to="/private/contact"
					className={({ isActive }) =>
						isActive ? 'text-red-500' : 'text-black'
					}
					end
				>
					Contact
				</NavLink>
			</nav>
			<Outlet />
		</>
	);
};
```

O también lo puedes asignar mediante sus hijos 

```tsx
<NavLink to="/message">
  {({ isActive }) => (
    <span className={isActive ? "active" : ""}>
      {isActive ? "👉" : ""} Tasks
    </span>
  )}
</NavLink>
```
## Tags

###### #React
###### #React-Router 