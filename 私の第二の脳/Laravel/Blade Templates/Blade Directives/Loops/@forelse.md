```php
@forelse ($users as $user)
    @continue($user->type == 1)

    <li>{{ $user->name }}</li>

    @break($user->number == 5)
@empty
    <p>No users found.</p>
@endforelse
```
## Tags

##### #Laravel