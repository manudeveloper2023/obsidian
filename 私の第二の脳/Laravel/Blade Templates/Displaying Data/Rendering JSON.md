Aveces quieres pasar un arreglo a tu vista con la intención de renderizarla como **JSON** para inicializar una variable de **JS**
## Ejemplo

```php
<script>
    var app = <?php echo json_encode($array); ?>;
</script>
```

También , puede usar el método de **`Illuminate\Support\Js::from`** que acepta los mismo argumentos que la función de **`json_encode`** , sin embargo, garantizará que el JSON resultante se escape correctamente para su inclusión dentro de comillas HTML

```php
<script>
    var app = {{ Illuminate\Support\Js::from($array) }};
</script>
```

Las ultimas versiones incluyen un facade de **`JS`** que proporciona acceso a esta funcionalidad dentro de las plantillas de blade

```php
<script>
    var app = {{ Js::from($array) }};
</script>
```
## Tags

##### #Laravel