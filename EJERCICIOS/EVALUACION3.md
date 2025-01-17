
## Práctica 4
### Data warehouse

Objetivo: Demostrar la identificación de los elementos que componen data warehouse y
su esquema

Ejercicio:

1. ¿Qué es un DataWarehouse?(valor 2)
-  Es un sistema que agrega y combina información de diferentes fuentes en un almacén de datos único y centralizado; consistente para respaldar el análisis empresarial, la minería de datos, inteligencia artificial y Machine Learning.
2. Realiza un diseño del modelo en estrella (valor 2)
![GestoresBD drawio](https://user-images.githubusercontent.com/102439815/173166061-ba01fcd1-8d13-479d-9220-abefe667e60a.png)
3. Realiza un diseño del modelo copo de nieve (valor 2)
![coponieve](https://user-images.githubusercontent.com/102439815/173168065-bdc44848-ec1f-4487-892f-40fa91825be4.png)
## Práctica 7
### Funciones en SQL
Objetivo: Demostrar el uso y aplicación en una base de datos para mejorar la gestión

Ejercicio:

1. Calcula el número total de productos que hay en la tabla productos. (valor 4.5)
- USE tienda_de_informatica;
- SELECT count(nombre_producto) FROM producto;
- ![image](https://user-images.githubusercontent.com/102439815/173168115-b1ecdfac-1c9c-4226-aa34-7b7ee899fcca.png)
2. Muestra el número total de productos que tiene cada uno de los fabricantes. El listado
también debe incluir los fabricantes que no tienen ningún producto. El resultado
mostrará dos columnas, una con el nombre del fabricante y otra con el número de
productos que tiene. Ordene el resultado descendentemente por el número de
productos. (valor 4.5)
- USE tienda_de_informatica;
- SELECT fabricante, count(fabricante) AS productos_por_fabricante
- FROM producto
- GROUP BY fabricante
- ORDER BY productos_por_fabricante;
- ![image](https://user-images.githubusercontent.com/102439815/173168772-5d552741-be2c-4c69-afab-e789d182728b.png)
3. Muestra el precio máximo, precio mínimo y precio medio de los productos de cada
uno de los fabricantes. El resultado mostrará el nombre del fabricante junto con los
datos que se solicitan. (valor 4.5)
- USE tienda_de_informatica;
- SELECT fabricante,
- MAX(precio) AS mayor_precio,
- MIN(precio) AS menor_precio,
- AVG(precio) As precio_medio
- FROM producto
- GROUP BY fabricante;
- ![image](https://user-images.githubusercontent.com/102439815/173169225-2e95b3cd-82c3-4b7e-800f-997bc0281e4d.png)
4. Muestra el nombre de cada fabricante, junto con el precio máximo, precio mínimo,
precio medio y el número total de productos de los fabricantes que tienen un precio
medio superior a 200€. Es necesario mostrar el nombre del fabricante. (valor 4.5)
- USE tienda_de_informatica;
- SELECT fabricante,
- MAX(precio) AS precio_maximo,
- MIN(precio) AS precio_minimo,
- AVG(precio) As precio_medio,
- count(fabricante) AS productos_por_fabricante
- FROM producto
- WHERE precio > 200
- GROUP BY fabricante;
- ![image](https://user-images.githubusercontent.com/102439815/173169512-3d9a6f67-c588-4c62-889d-353e5399eda1.png)
- https://www.db-fiddle.com/f/rWjbX1m3LiQzUHSVS862n5/2


