Si todo tu grupo de rutas usa el mismo controlador , tu puedes usar su método de fachada de **`Route::controller`** , para agruparlos

```php
use App\Http\Controllers\OrderController;
 
Route::controller(OrderController::class)->group(function () {
    Route::get('/orders/{id}', 'show');
    Route::post('/orders', 'store');
});
```

## Tags

##### #Laravel