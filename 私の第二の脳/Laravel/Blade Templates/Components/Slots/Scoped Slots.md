Puedes acceder al componente dentro de la ranura de `$component`

```php
// app/View/Components/AlertComponent.php
namespace App\View\Components;

use Illuminate\View\Component;

class AlertComponent extends Component
{
    public $type;
    public $message;

    public function __construct($type, $message)
    {
        $this->type = $type;
        $this->message = $message;
    }

    // Public method to format the alert message
    public function formatAlert()
    {
        return strtoupper($this->message);
    }

    public function render()
    {
        return view('components.alert');
    }
}
```

```php
<x-button>
    <x-slot:title>
        {{ $component->formatAlert('Hello from Button') }}
    </x-slot>
</x-button>
```

```php
<button class="p-4 bg-black text-white rounded-lg">
    {{ $title }}
</button>
```
## Tags

##### #Laravel