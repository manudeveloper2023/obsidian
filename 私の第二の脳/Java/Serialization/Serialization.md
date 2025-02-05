Es la conversión del   de un objeto a un flujo de bytes.Realiza una `conversión` de un objeto `Java` en un flujo estático de bytes , que podemos guardar en una `base de datos`

## Ejemplo

Implementamos la interfaz `Serializable` a la clase `Dog`

```php
class Dog implements Serializable {
    private String name;
    private int age;

    public Dog(String name, int age) {
        this.name = name;
        this.age = age;
    }

```

Sucesivamente , utilizamos los metodos de las clases de `FileOutputStream` y `ObjectOutputStream`

- `FileOutputStream` : Es un flujo de salida que se utiliza para escribir datos en un archivo.
- `ObjectOutputStream` : Subclase de `FileOutputStream` que se utiliza para serializar objetos

```php
public static void serializeObjectToText(Object obj, String path) {  
    try (FileOutputStream fout = new FileOutputStream(path);  
         ObjectOutputStream out = new ObjectOutputStream(fout)) {  

		// Transforma el objeto a una secuencia de bytes
		
        out.writeObject(obj);  
        System.out.println("Object " + obj.getClass().getSimpleName() + " has been serialized");  
    } catch (IOException e) {  
        System.out.println(e.getMessage());  
    }}
```
## Tags

##### #Java 
##### #Java-Serialization