Al definir una vista hijo , puedes usar `@extends` para especificar que `layout` del hijo debe heredar la vista secundaria

```php
<!-- resources/views/child.blade.php -->
 
@extends('layouts.app')
 
@section('title', 'Page Title')
 
@section('sidebar')
    @parent
 
    <p>This is appended to the master sidebar.</p>
@endsection
 
@section('content')
    <p>This is my body content.</p>
@endsection
```
## Tags

##### #Laravel
##### #Laravel-Blade