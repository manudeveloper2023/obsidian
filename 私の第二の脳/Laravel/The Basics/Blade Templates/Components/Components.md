Para crear un componente , puedes usar el comando de `make:component`

```bash
php artisan make:component Alert
```

Lo que te creara una vista en `resources/views/components` y cuando estes escribiendo componentes de tu propia aplicación , también se creara una clase en `App/View/Components`

También , lo puedes crear dentro de subdirectorios

```bash
php artisan make:component Forms/Input
```

Creara un componente de `Input` en el `app/View/Components/Forms` y la vista sera colocada en `resources/views/components/forms`

Si lo quieres crear de manera anónima sin crear ninguna clase , puedes usar `--view`

```bash
php artisan make:component forms.input --view
```

Por lo que , para renderizar el componente puedes usar `<x-forms.input />`
## Tags

##### #Laravel