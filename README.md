   <h4>Consultas sobre una tabla</h4>

<h4>1. Lista el nombre de todos los productos que hay en la tabla producto .</h4>

    SELECT nombre
    FROM producto;

<h4>2. Lista los nombres y los precios de todos los productos de la tabla producto .</h4>

    SELECT nombre,precio
    FROM producto;

<h4>3. Lista todas las columnas de la tabla producto .</h4>

    SELECT id,nombre,precio,id_fabricante
    FROM producto;

<h4>4. Lista el nombre de los productos, el precio en euros y el precio en dólares estadounidenses
(USD).</h4>

    SELECT nombre,precio, TRUNCATE((precio *1.07),2) AS precio_dolar
    FROM producto;

<h4>5. Lista el nombre de los productos, el precio en euros y el precio en dólares estadounidenses
(USD). Utiliza los siguientes alias para las columnas: nombre de producto , euros , dólares .</h4>

    SELECT nombre AS 'nombre de producto',precio AS euros,TRUNCATE((precio*1.07),2) AS dolares
    FROM producto;

<h4>6. Lista los nombres y los precios de todos los productos de la tabla producto , convirtiendo los
nombres a mayúscula.</h4>

    SELECT UPPER(nombre),precio
    FROM producto;

<h4>7. Lista los nombres y los precios de todos los productos de la tabla producto , convirtiendo los
nombres a minúscula.</h4>

    SELECT UPPER(nombre),precio
    FROM producto;

<h4>8. Lista el nombre de todos los fabricantes en una columna, y en otra columna obtenga en
mayúsculas los dos primeros caracteres del nombre del fabricante.</h4>

    SELECT nombre AS nombre_fabricante, UPPER(SUBSTRING(nombre,1,2)) AS iniciar
    FROM fabricante;

<h4>9. Lista los nombres y los precios de todos los productos de la tabla producto , redondeando el
valor del precio.</h4>

    SELECT nombre,FLOOR(precio)
    FROM producto;

<h4>10. Lista los nombres y los precios de todos los productos de la tabla producto , truncando el
valor del precio para mostrarlo sin ninguna cifra decimal.</h4>

    SELECT nombre,TRUNCATE(precio,0) AS precio
    FROM producto;

<h4>11. Lista el identificador de los fabricantes que tienen productos en la tabla producto .</h4>

    SELECT id_fabricante
    FROM producto;

<h4>12. Lista el identificador de los fabricantes que tienen productos en la tabla producto ,
eliminando los identificadores que aparecen repetidos.</h4>

    SELECT DISTINCT id_fabricante
    FROM producto;

<h4>13. Lista los nombres de los fabricantes ordenados de forma ascendente.</h4>

    SELECT nombre 
    FROM fabricante
    ORDER BY nombre;

<h4>14. Lista los nombres de los fabricantes ordenados de forma descendente.</h4>

    SELECT nombre 
    FROM fabricante
    ORDER BY nombre DESC;

<h4>15. Lista los nombres de los productos ordenados en primer lugar por el nombre de forma
ascendente y en segundo lugar por el precio de forma descendente.</h4>

    SELECT nombre,precio
    FROM producto
    ORDER BY nombre;

    SELECT nombre,precio
    FROM producto
    ORDER BY precio DESC;

<h4>16. Devuelve una lista con las 5 primeras filas de la tabla fabricante .</h4>

    SELECT id,nombre
    FROM fabricante
    LIMIT 5;

<h4>17. Devuelve una lista con 2 filas a partir de la cuarta fila de la tabla fabricante . La cuarta fila
también se debe incluir en la respuesta.</h4>

    SELECT id,nombre
    FROM fabricante
    LIMIT 3,2;

<h4>18. Lista el nombre y el precio del producto más barato. (Utilice solamente las cláusulas ORDER
BY y LIMIT )</h4>

    SELECT nombre,precio
    FROM producto
    ORDER BY precio
    LIMIT 1;

<h4>19. Lista el nombre y el precio del producto más caro. (Utilice solamente las cláusulas ORDER BY
y LIMIT )</h4>

    SELECT nombre,precio
    FROM producto
    ORDER BY precio DESC
    LIMIT 1; 

<h4>20. Lista el nombre de todos los productos del fabricante cuyo identificador de fabricante es
igual a 2.</h4>

    SELECT nombre,precio,id_fabricante
    FROM producto
    WHERE id_fabricante = 2;

<h4>21. Lista el nombre de los productos que tienen un precio menor o igual a 120€.</h4>

    SELECT nombre,precio,id_fabricante
    FROM producto
    WHERE precio<=120;

<h4>22. Lista el nombre de los productos que tienen un precio mayor o igual a 400€.</h4>
 
    SELECT nombre,precio,id_fabricante
    FROM producto
    WHERE precio>=400;

<h4>23. Lista el nombre de los productos que no tienen un precio mayor o igual a 400€.BETWEEN .</h4>

    SELECT nombre,precio,id_fabricante
    FROM producto
    WHERE NOT precio<400;

<h4>24. Lista todos los productos que tengan un precio entre 80€ y 300€. Sin utilizar el operador
BETWEEN .</h4>

    SELECT nombre,precio
    FROM producto
    WHERE (precio>80) AND (precio<=300);

<h4>25. Lista todos los productos que tengan un precio entre 60€ y 200€. Utilizando el operador
fabricante sea igual a 6.</h4>
    
    SELECT nombre,precio
    FROM producto
    WHERE precio BETWEEN 60 AND 200;

<h4>26. Lista todos los productos que tengan un precio mayor que 200€ y que el identificador de
operador IN .</h4>

    SELECT nombre,precio,id_fabricante
    FROM producto
    WHERE precio > 200 AND id_fabricante;

<h4>27. Lista todos los productos donde el identificador de fabricante sea 1, 3 o 5. Sin utilizar el
operador IN .</h4>



<h4>28. Lista todos los productos donde el identificador de fabricante sea 1, 3 o 5. Utilizando el
valor del precio). Cree un alias para la columna que contiene el precio que se llame centimos.</h4>



<h4>29. Lista el nombre y el precio de los productos en céntimos (Habrá que multiplicar por 100 el
céntimos .</h4>



<h4>31. Lista los nombres de los fabricantes cuyo nombre termine por la vocal e .</h4>



<h4>30. Lista los nombres de los fabricantes cuyo nombre empiece por la letra S .</h4>



<h4>32. Lista los nombres de los fabricantes cuyo nombre contenga el carácter w .</h4>



<h4>33. Lista los nombres de los fabricantes cuyo nombre sea de 4 caracteres.</h4>



<h4>34. Devuelve una lista con el nombre de todos los productos que contienen la cadena Portátil
en el nombre.</h4>



<h4>35. Devuelve una lista con el nombre de todos los productos que contienen la cadena Monitor
en el nombre y tienen un precio inferior a 215 €.</h4>



<h4>36. Lista el nombre y el precio de todos los productos que tengan un precio mayor o igual a
180€. Ordene el resultado en primer lugar por el precio (en orden descendente) y en
segundo lugar por el nombre (en orden ascendente).</h4>


