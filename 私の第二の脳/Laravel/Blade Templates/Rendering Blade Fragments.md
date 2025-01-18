Si utilizar `frontend frameworks` , puedes ocasionalmente necesitar una porción de `blade` dentro de tu `HTTP Response`.`Blade` permite crear fragmentos

```php
@fragment('user-list')
    <ul>
        @foreach ($users as $user)
            <li>{{ $user->name }}</li>
        @endforeach
    </ul>
@endfragment
```
## Tags

##### #Laravel
##### #Laravel-Blade