Para pequeños componentes , puedes usarlos con un `markup` desde el renderizado

```PHP
/**
 * Get the view / contents that represent the component.
 */
public function render(): string
{
    return <<<'blade'
        <div class="alert alert-danger">
            {{ $slot }}
        </div>
    blade;
}
```

## Tags

##### #Laravel