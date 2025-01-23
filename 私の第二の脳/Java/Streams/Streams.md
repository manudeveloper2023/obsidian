Un **stream** en Java es una secuencia de elementos que permite realizar operaciones de manera funcional y declarativa sobre una colección de datos

## Ejemplo

```java
import java.util.Arrays;
import java.util.List;

public class StreamExample {
    public static void main(String[] args) {
        List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);

        int result = numbers.stream()           // Convierte la lista en un Stream
                            .filter(n -> n % 2 == 0)  // Filtra solo los números pares
                            .map(n -> n * 2)          // Multiplica cada número por 2
                            .reduce(0, Integer::sum); // Suma los números

        System.out.println("Resultado: " + result);  // Imprime: 12
    }
}
```
## Tags

##### #Java

