Si quieres combinar ciclos y `incluir` en una sola linea puedes usar la directiva de `@each`

```php

<div class="grid md:grid-cols-2 gap-12">
        @each('components.card', $cards, 'card' , 'components.card.empty')
</div>

// Card Component

<div class="flex flex-col p-4 shadow-md rounded-lg ">
    <h2 class="text-2xl font-bold">{{ $card['title'] }}</h2>
    <p class="text-gray-700">{{ $card['text'] }}</p>
</div>

// Si no hay cartas , se renderizara esto

<p>There are no Cards</p>

```
## Tags

##### #Laravel