
Los fabricantes que actualmente no tienen ningún producto no aparecerán en el resultado, ya que se trata de una unión interna. Si quisiéramos incluir los nombres de dichos fabricantes en el resultado, podríamos hacer lo siguiente:


```postgresql
SELECT m.name AS mname, pname
FROM manufacturers m LEFT JOIN LATERAL get_product_names(m.id) pname ON true;
```

Una recursividad para determinar los arboles de jerarquia entre los diferentes segmento de los empleados

```postgresql
WITH RECURSIVE employee_recursive(distance, employee_name, manager_name) AS (
    SELECT 1, employee_name, manager_name
    FROM employee
    WHERE manager_name = 'Mary'
  UNION ALL
    SELECT er.distance + 1, e.employee_name, e.manager_name
    FROM employee_recursive er, employee e
    WHERE er.employee_name = e.manager_name
  )
SELECT distance, employee_name FROM employee_recursive;
```
## Tags

###### #Postgresql
###### #SQL