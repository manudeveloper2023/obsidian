Para verificar el método del `request` , puedes usar `isMethod` para veríficar el verbo de HTTP 

```PHP
$method = $request->method();
 
if ($request->isMethod('post')) {
    // ...
}
```
## Tags

##### #Laravel
##### #Laravel-Request