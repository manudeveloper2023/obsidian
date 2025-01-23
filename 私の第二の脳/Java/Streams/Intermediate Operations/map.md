Transforma cada elemento dentro del `stream` en otra forma usando una función

## Ejemplo

```java
List<Employee> increased =
                employees.stream().map(employee-> new Employee(
                employee.getFirstName(),
                employee.getLastName(),
                employee.getSalary() * 1.1,
                employee.getProjects()
                )).toList();
```
## Tags

##### #Java
