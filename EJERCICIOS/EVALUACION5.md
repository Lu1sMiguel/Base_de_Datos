## Práctica 9.
### Operaciones en una base de datos.
Objetivo: Demostrar las operaciones que se realizan en una base de datos, aplicar el modelo relacional y el lenguaje SQL

Evaluación: Para poder tener correcto cada ejercicio deberán de mostrar el resultado que se da en cada respuesta.

Lista el nombre de todos los productos que hay en la tabla producto.


1. Lista los nombres y los precios de todos los productos de la tabla producto.
- USE tienda_de_informatica;
- SELECT nombre_producto, precio
- FROM producto;
- ![image](https://user-images.githubusercontent.com/102439815/173169759-ad9190cf-aa80-4763-84dc-02388dab95fc.png)
2. Lista todas las columnas de la tabla producto.
- USE tienda_de_informatica;
- SELECT *
- FROM producto;
- ![image](https://user-images.githubusercontent.com/102439815/173169822-d6979e2e-c71b-45bb-b384-14096d7bc562.png)
3. Devuelve una lista con el nombre del producto, precio y nombre de fabricante de
todos los productos de la base de datos.
- USE tienda_de_informatica;
- SELECT nombre_producto, precio, fabricante
- FROM producto;
- ![image](https://user-images.githubusercontent.com/102439815/173170017-17ae8eea-8dec-4ce2-9271-0ba38ace7233.png)

Subconsultas (En la cláusula WHERE)
1. Devuelve todos los productos del fabricante Lenovo. (Sin utilizar INNER
JOIN).
- USE tienda_de_informatica;
- SELECT nombre_producto, fabricante
- FROM producto
- WHERE fabricante='LENOVO';
- ![image](https://user-images.githubusercontent.com/102439815/173170150-c48b5dca-02e9-43a0-baff-50f9313cb85d.png)
2. Devuelve todos los datos de los productos que tienen el mismo precio que el
producto más caro del fabricante Lenovo. (Sin utilizar INNER JOIN).
- USE tienda_de_informatica;
- SELECT *
- FROM producto
- WHERE precio = (SELECT MAX(precio) FROM producto WHERE fabricante='LENOVO');
- ![image](https://user-images.githubusercontent.com/102439815/173170513-fc77d5d9-eab0-49d4-8022-3be15ea21b5a.png)
3. Lista el nombre del producto más caro del fabricante Lenovo.
- USE tienda_de_informatica;
- SELECT nombre_producto AS producto_mas_caro_LENOVO
- FROM producto
- WHERE precio = (SELECT MAX(precio) FROM producto WHERE fabricante = 'LENOVO');
- ![image](https://user-images.githubusercontent.com/102439815/173170905-d3ad01ac-14d9-4319-85b6-9288b2265925.png)

https://www.db-fiddle.com/f/rWjbX1m3LiQzUHSVS862n5/3
