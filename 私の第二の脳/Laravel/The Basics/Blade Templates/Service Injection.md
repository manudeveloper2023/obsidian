Puedes usar la directiva de `@inject` para agregarlo con un `service container`

```php
@inject('metrics', 'App\Services\MetricsService')
 
<div>
    Monthly Revenue: {{ $metrics->monthlyRevenue() }}.
</div>
```
## Tags

##### #Laravel
##### #Laravel-Blade