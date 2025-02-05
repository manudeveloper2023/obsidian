Permite pasar una solicitud a lo large de una cadena de `manejadores`

Al recibir una solicitud, cada manejador decide `si la procesa o si la pasa al siguiente manejador de la cadena`.

![[Pasted image 20250130155101.png]]

## UML

![[Pasted image 20250130155119.png]]

## Ejemplo

```java
// middleware

public abstract class Middleware {
    private Middleware next;

    public static Middleware link(Middleware first , Middleware ... chain){
        Middleware head = first;
        for (Middleware nextInChain : chain){
            head.next = nextInChain;
            head = nextInChain;
        }
        return first;
    }

    public abstract  Boolean check();
    protected Boolean handle(){
        if(next == null) return true;
        return next.check();
    }
}
```

```java
// DogHasANameStartWithAHandler

public class DogHasANameStartWithA extends  Middleware{
    private final String dogName;
    public DogHasANameStartWithA(String dogName){
        this.dogName = dogName;
    }
    public Boolean check(){
        if(dogName.startsWith("A")){
            return handle();
        }
        return false;
    }

}
```

```java
// DogHasMoreThat4YearsHandler

public class DogHasMoreThat4Years extends Middleware{
    private final Integer dogYears;
    public DogHasMoreThat4Years(Integer dogYears){
        this.dogYears = dogYears;
    }

    public Boolean check(){
        if(dogYears > 4){
            return handle();
        }
        return false;
    }
}
```

```java
// main

public class Main {
    private Middleware middleware;
    
    public Main() {
        this.middleware = Middleware.link(new DogHasMoreThat4Years(5), new DogHasANameStartWithA("A"));
    }

    public static void main(String[] args) {
        Main app = new Main();

        if (app.middleware.check()) {
            System.out.println("The dog is valid");
        } else {
            System.out.println("The dog is not valid");
        }
    }
}
```
## Tags

##### #Design-Patterns