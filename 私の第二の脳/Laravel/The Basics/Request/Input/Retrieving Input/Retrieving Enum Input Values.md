Para usar los `PHP enums` pueden ser recuperados de la `request` con el tipo de `ENUM`

```php
use App\Enums\Status;

$status = $request->enum('status', Status::class);
```

Si el `input value` es una matriz de valores que corresponde a un `ENUM PHP` , puede usar el método de `enums`

```php
use App\Enums\Product;
 
$products = $request->enums('products', Product::class);
```
## Tags

##### #Laravel
##### #Laravel-Request