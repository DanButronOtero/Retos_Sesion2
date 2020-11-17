# Reto 1

## ¿Qué artículos incluyen la palabra Pasta en su nombre?
```sql
select  * from articulo where nombre like '%Pasta%'; 
```

![](img/r1-1.png)



## ¿Qué artículos incluyen la palabra Cannelloni en su nombre?
```sql
select  * from articulo where nombre like '%Cannelloni%';
```

 ![](img/r1-2.png)



## ¿Qué nombres están separados por un guión (-) por ejemplo Puree - Kiwi?
```sql
select  * from articulo where nombre like '% - %';
```

![](img/r1-3.png)

## ¿Qué puestos incluyen la palabra Designer?
```sql
select * from puesto where nombre like '%Designer%';
```

![](img/r1-4.png)

## ¿Qué puestos incluyen la palabra Developer?
```sql
select * from puesto where nombre like '%Developer%';
```

![](img/r1-5.png)

# Reto 2


## ¿Cuál es el promedio de salario de los puestos?
```sql
select avg(p.salario) as promedio from puesto p ;
```

![](img/r2-1.png)

## ¿Cuántos artículos incluyen la palabra Pasta en su nombre?
``` sql
select count(id_articulo) from articulo where nombre like '%Pasta%';
```

![](img/r2-2.png)

## ¿Cuál es el salario mínimo y máximo?
``` sql
select max(salario) as SALARIO_MAXIMO,min(salario) as SALARIO_MINIMO from puesto;
```

![](img/r2-3.png)

## ¿Cuál es la suma del salario de los últimos cinco puestos agregados?
```sql
select sum(suma.salario) as 'SUMA ultimos 5'
from (select salario from puesto
      order by id_puesto desc limit 5) as suma; 
```

![](img/r2-4.png)

