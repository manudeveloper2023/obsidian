Al transmitir datos al cliente a medida que se generan , pueden reducir significativamente la memoria y mejorar el rendimiento , mayormente en respuestas muy grandes

Las respuestas transmitidas permiten que el cliente comience a procesar los datos antes de que el servidor haya terminado de enviarlos

```php
function streamedContent(): Generator {
    yield 'Hello, ';
    yield 'World!';
}
 
Route::get('/stream', function () {
    return response()->stream(function (): void {
    foreach (streamedContent() as $chunk) {
        echo $chunk; // Envía el trozo de datos al cliente
        ob_flush();   // Asegura que el contenido se haya enviado al navegador
        flush();      // Libera el buffer de salida
        sleep(2);     // Simula una demora entre los trozos
    }
}, 200, ['X-Accel-Buffering' => 'no']);
});
```
## Tags

##### #Laravel
##### #Laravel-Response