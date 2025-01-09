Se utiliza para verificar si una sección específica está definida en la vista

```php
@hasSection('navigation')
    <div class="pull-right">
        @yield('navigation')
    </div>

    <div class="clearfix"></div>
@endif
```

## Tags

##### #Laravel