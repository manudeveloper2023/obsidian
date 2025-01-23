Sirve para filtrar resultados basados en una condición específica

```php
List<String> filterEmployee =
                increasedEmployees
                .stream()
                .filter(employee -> employee.getSalary() > 2000)
                .map(Employee::getFirstName)
                .toList();
```
## Tags

##### #Java