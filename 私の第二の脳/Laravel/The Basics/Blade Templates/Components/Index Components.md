A veces , quieres componetizar tu componente en un grupo de componentes y es posible que quieras agrupar los `componentes relacionados` dentro de un directorio

```php
App\Views\Components\Card\Card
App\Views\Components\Card\Header
App\Views\Components\Card\Body
```

Lo cual podemos mostrarlo así , para renderizarlo

```php
<x-card> // No se realiza x-card.card , por que Laravel reconoce cual es la vista raiz
    <x-card.header>...</x-card.header>
    <x-card.body>...</x-card.body>
</x-card>
```
## Tags

##### #Laravel