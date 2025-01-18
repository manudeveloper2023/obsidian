```php
<!-- resources/views/components/layout.blade.php -->
 
<html>
    <head>
        <title>{{ $title ?? 'Todo Manager' }}</title>
    </head>
    <body>
        <h1>Todos</h1>
        <hr/>
        {{ $slot }}
    </body>
</html>
```

Una vez , que tenemos el componente del `layout` , podemos crear una vista de `blade` , que utilicen el componente

```php
<!-- resources/views/tasks.blade.php -->
 
<x-layout>
    <x-slot:title>
        Custom Title
    </x-slot>
 
    @foreach ($tasks as $task)
        <div>{{ $task }}</div>
    @endforeach
</x-layout>
```

Puedes definirlo mediante las rutas de 

```php
use App\Models\Task;
 
Route::get('/tasks', function () {
    return view('tasks', ['tasks' => Task::all()]);
});
```
## Tags

##### #Laravel
##### #Laravel-Blade

