La directiva de `@section` , define la sección del contenido ,mientras que `@yield` es usado para mostrar el contenido de una sección

```php
<!-- resources/views/layouts/app.blade.php -->
 
<html>
    <head>
        <title>App Name - @yield('title')</title>
    </head>
    <body>
        @section('sidebar')
            This is the master sidebar.
        @show
 
        <div class="container">
            @yield('content')
        </div>
    </body>
</html>
```
## Tags

##### #Laravel
##### #Laravel-Blade
