   <h2>Consultas sobre una tabla</h2>

<h3>1. Lista el nombre de todos los productos que hay en la tabla producto .</h3>

```sql
    SELECT nombre
    FROM producto;
```
<h3>2. Lista los nombres y los precios de todos los productos de la tabla producto .</h3>

```sql
    SELECT nombre,precio
    FROM producto;
```
<h3>3. Lista todas las columnas de la tabla producto .</h3>

```sql
    SELECT id,nombre,precio,id_fabricante
    FROM producto;
```
<h3>4. Lista el nombre de los productos, el precio en euros y el precio en dólares estadounidenses
(USD).</h3>

```sql
    SELECT nombre,precio, TRUNCATE((precio *1.07),2) AS precio_dolar
    FROM producto;
```
<h3>5. Lista el nombre de los productos, el precio en euros y el precio en dólares estadounidenses
(USD). Utiliza los siguientes alias para las columnas: nombre de producto , euros , dólares .</h3>

```sql
    SELECT nombre AS 'nombre de producto',precio AS euros,TRUNCATE((precio*1.07),2) AS dolares
    FROM producto;
```
<h3>6. Lista los nombres y los precios de todos los productos de la tabla producto , convirtiendo los
nombres a mayúscula.</h3>

```sql
    SELECT UPPER(nombre),precio
    FROM producto;
```
<h3>7. Lista los nombres y los precios de todos los productos de la tabla producto , convirtiendo los
nombres a minúscula.</h3>

```sql
    SELECT UPPER(nombre),precio
    FROM producto;
```
<h3>8. Lista el nombre de todos los fabricantes en una columna, y en otra columna obtenga en
mayúsculas los dos primeros caracteres del nombre del fabricante.</h3>

```sql
    SELECT nombre AS nombre_fabricante, UPPER(SUBSTRING(nombre,1,2)) AS iniciar
    FROM fabricante;
```
<h3>9. Lista los nombres y los precios de todos los productos de la tabla producto , redondeando el
valor del precio.</h3>

```sql
    SELECT nombre,FLOOR(precio)
    FROM producto;
```
<h3>10. Lista los nombres y los precios de todos los productos de la tabla producto , truncando el
valor del precio para mostrarlo sin ninguna cifra decimal.</h3>

```sql
    SELECT nombre,TRUNCATE(precio,0) AS precio
    FROM producto;
```
<h3>11. Lista el identificador de los fabricantes que tienen productos en la tabla producto .</h3>

```sql
    SELECT id_fabricante
    FROM producto;
```
<h3>12. Lista el identificador de los fabricantes que tienen productos en la tabla producto ,
eliminando los identificadores que aparecen repetidos.</h3>

```sql
    SELECT DISTINCT id_fabricante
    FROM producto;
```
<h3>13. Lista los nombres de los fabricantes ordenados de forma ascendente.</h3>

```sql
    SELECT nombre 
    FROM fabricante
    ORDER BY nombre;
```
<h3>14. Lista los nombres de los fabricantes ordenados de forma descendente.</h3>

```sql
    SELECT nombre 
    FROM fabricante
    ORDER BY nombre DESC;
```
<h3>15. Lista los nombres de los productos ordenados en primer lugar por el nombre de forma
ascendente y en segundo lugar por el precio de forma descendente.</h3>

```sql
    SELECT nombre,precio
    FROM producto
    ORDER BY nombre;

    SELECT nombre,precio
    FROM producto
    ORDER BY precio DESC;
```
<h3>16. Devuelve una lista con las 5 primeras filas de la tabla fabricante .</h3>

```sql
    SELECT id,nombre
    FROM fabricante
    LIMIT 5;
```
<h3>17. Devuelve una lista con 2 filas a partir de la cuarta fila de la tabla fabricante . La cuarta fila
también se debe incluir en la respuesta.</h3>

```sql
    SELECT id,nombre
    FROM fabricante
    LIMIT 3,2;
```
<h3>18. Lista el nombre y el precio del producto más barato. (Utilice solamente las cláusulas ORDER
BY y LIMIT )</h3>

```sql
    SELECT nombre,precio
    FROM producto
    ORDER BY precio
    LIMIT 1;
```
<h3>19. Lista el nombre y el precio del producto más caro. (Utilice solamente las cláusulas ORDER BY
y LIMIT )</h3>

```sql
    SELECT nombre,precio
    FROM producto
    ORDER BY precio DESC
    LIMIT 1; 
```
<h3>20. Lista el nombre de todos los productos del fabricante cuyo identificador de fabricante es
igual a 2.</h3>

```sql
    SELECT nombre,precio,id_fabricante
    FROM producto
    WHERE id_fabricante = 2;
```
<h3>21. Lista el nombre de los productos que tienen un precio menor o igual a 120€.</h3>

```sql
    SELECT nombre,precio,id_fabricante
    FROM producto
    WHERE precio<=120;
```
<h3>22. Lista el nombre de los productos que tienen un precio mayor o igual a 400€.</h3>
 
```sql
    SELECT nombre,precio,id_fabricante
    FROM producto
    WHERE precio>=400;
```
<h3>23. Lista el nombre de los productos que no tienen un precio mayor o igual a 400€.BETWEEN .</h3>

```sql
    SELECT nombre,precio,id_fabricante
    FROM producto
    WHERE NOT precio<400;
```
<h3>24. Lista todos los productos que tengan un precio entre 80€ y 300€. Sin utilizar el operador
BETWEEN .</h3>

```sql
    SELECT nombre,precio
    FROM producto
    WHERE (precio>80) AND (precio<=300);
```
<h3>25. Lista todos los productos que tengan un precio entre 60€ y 200€. Utilizando el operador
fabricante sea igual a 6.</h3>
    
```sql
    SELECT nombre,precio
    FROM producto
    WHERE precio BETWEEN 60 AND 200;
```
<h3>26. Lista todos los productos que tengan un precio mayor que 200€ y que el identificador de
operador IN .</h3>

```sql
    SELECT nombre,precio,id_fabricante
    FROM producto
    WHERE precio > 200 AND id_fabricante;
```
<h3>27. Lista todos los productos donde el identificador de fabricante sea 1, 3 o 5. Sin utilizar el
operador IN .</h3>

```sql

```
<h3>28. Lista todos los productos donde el identificador de fabricante sea 1, 3 o 5. Utilizando el
valor del precio). Cree un alias para la columna que contiene el precio que se llame centimos.</h3>


```sql
```
<h3>29. Lista el nombre y el precio de los productos en céntimos (Habrá que multiplicar por 100 el
céntimos .</h3>

```sql

```
<h3>31. Lista los nombres de los fabricantes cuyo nombre termine por la vocal e .</h3>

```sql

```
<h3>30. Lista los nombres de los fabricantes cuyo nombre empiece por la letra S .</h3>


```sql
```
<h3>32. Lista los nombres de los fabricantes cuyo nombre contenga el carácter w .</h3>


```sql
```
<h3>33. Lista los nombres de los fabricantes cuyo nombre sea de 4 caracteres.</h3>


```sql
```
<h3>34. Devuelve una lista con el nombre de todos los productos que contienen la cadena Portátil
en el nombre.</h3>


```sql
```
<h3>35. Devuelve una lista con el nombre de todos los productos que contienen la cadena Monitor
en el nombre y tienen un precio inferior a 215 €.</h3>

```sql

```
<h3>36. Lista el nombre y el precio de todos los productos que tengan un precio mayor o igual a
180€. Ordene el resultado en primer lugar por el precio (en orden descendente) y en
segundo lugar por el nombre (en orden ascendente).</h3>


```sql
```