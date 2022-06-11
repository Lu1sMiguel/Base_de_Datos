## Práctica 3.
### Introducción a SQL
Objetivo: Demostrar la correcta identificación de los conceptos del lenguaje SQL
Ejercicio:

1. Menciona los comandos DMl: (valor .85)
- SELECT 
- INSERT 
- UPDATE 
- DELETE
2. Menciona 3 tipos de datos que existen: (valor .85)
- char(n) y varchar(n): cadena de caracteres de longitud fija y variable. 
- int, smallint y bigint: un entero, un entero pequeño y un entero grande.
- float(n): un número de coma flotante.
3. ¿Qué diferencia existe entre TRUNCATE y DELETE?(valor .85)
- TRUNCATE elimina todas las filas de la tabla sin borrar la tabla y resetea los contadores de auto incremento a 0. 
- SELECT borra la estructura de la tabla.
4. ¿Para qué se utiliza el atributo UNIQUE?(valor .85)
- Da un atributo a los campos en los que se requiera se tengan datos que no se puedan repetir.
5. ¿Qué diferencia hay entre los tipos de datos VARCHAR y CHAR? (valor .85)
- CHAR es una cadena de caracteres de longitud fija.
- VARCHAR es una cadena de caracteres de longitud variable.
6. Defina brevemente el significado de las siglas SQL(valor .85)
- Lenguaje de consulta estructurada.
7. Defina brevemente qué es MySQL WorkBench (valor .85)
- Un editor visual de base de datos MySQ y que se caracteriza por su editor de diagramas.

## Práctica 5.
### Gestores de base de datos

Objetivo: Categorizar los distintos gestores de base de datos que existen y señalar las
ventajas y desventajas

Evaluación: Conoce los tipos de gestores de base de datos 3 puntos.

Domina sus diferencias de los gestores de base de datos mencionados 3 puntos

Ejercicio:

En un mapa conceptual presenta 3 gestores de bases de datos, sus características
principales, las ventajas y desventajas. (valor 6)

![Untitled Diagram drawio](https://user-images.githubusercontent.com/102439815/173160826-51cc50a9-4958-474f-bc4d-b037bf819486.png)

## Práctica 6.
### Herramienta en línea y ejercicio necesarios para realizar las prácticas

Creación de base de datos.

Objetivo: Demostrar mediante la creación de una base de datos el uso y la aplicación de
las funciones

Ejercicio: Creación de la base de datos (valor 18 puntos)

Tienda de informática

![image](https://user-images.githubusercontent.com/91554777/170415101-717bca19-3644-46a9-8a57-8d5940c5d283.png)


Modelo entidad/relación

![GestoresBD drawio](https://user-images.githubusercontent.com/102439815/173164874-1bd57dc1-dd7e-4135-a553-9b88f4e63cd0.png)


Base de datos para MySQL
- 1 CREATE DATABASE tienda_de_informatica;
- 2 
- 3 USE tienda_de_informatica;
- 4 CREATE TABLE producto(
- 5 codigo char(5) PRIMARY KEY,
- 6 producto varchar(50) NOT NULL UNIQUE,
- 7 precio float NOT NULL,
- 8 fabricante VARCHAR(100)
- 9 );
- 10 INSERT INTO producto VALUES ('DD-23','Disco duro Sata3 1TB',86.99,'SEAGATE');
- 11 INSERT INTO producto VALUES ('MM-34','Memoria RAM DDR4 8GB',120.6,'CRUCIAL');
- 12 INSERT INTO producto VALUES ('DD-98','Disco SSD 1 TB',150.99,'SAMSUNG');
- 13 INSERT INTO producto VALUES ('MM-98','GEFORCE GTX1050Ti',185.7,'GIGABYTE');
- 14 INSERT INTO producto VALUES ('MM-23','GEFORCE GTX1080 Xtreme',755.6,'CRUCIAL');
- 15 INSERT INTO producto VALUES ('MT-12','MONITOR 24 LED Full HD',202.1,'ASUS');
- 16 INSERT INTO producto VALUES ('MT-08','MONITOR 27 LED Full HD',245.99,'ASUS');
- 17 INSERT INTO producto VALUES ('LP-19','Portátil Yoga 520',559.2,'LENOVO');
- 18 INSERT INTO producto VALUES ('LP-11','Portátil Ideapad 320',444.2,'LENOVO');
- 19 INSERT INTO producto VALUES ('IM-56','Impresora HP Deskjet 3720',59.99,'HP');
- 20 INSERT INTO producto VALUES ('IP-54','Impresora HP Laserjet Pro M26nw',180.3,'HP');

![image](https://user-images.githubusercontent.com/102439815/173164043-83a4e8e3-8522-4ddd-a48f-cef24f2a3ea3.png)

https://www.db-fiddle.com/f/pa2UujZUu1YfLMVe1KcvG1/1
