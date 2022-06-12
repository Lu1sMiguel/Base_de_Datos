## Práctica 8.
### Disparadores (Triggers)

Objetivo: Demostrar las operaciones que se realizan en una base de datos.

Ejercicio: Crea una base de datos llamada test que contenga una tabla llamada
alumnos con las siguientes columnas. (valor 18)

Evaluación:

Creación de la base de datos : 9 puntos.

https://www.db-fiddle.com/f/daHFtUzr2dPMXEx2QWoNKf/0

Creación de los Disparadores(Triggers): 9 puntos.

Tabla alumnos:

● id (entero sin signo)

● nombre (cadena de caracteres)

● apellido1 (cadena de caracteres)

● apellido2 (cadena de caracteres)

● nota (número real)

Una vez creada la tabla escriba dos triggers con las siguientes características:

● Trigger 1: trigger_check_nota_before_insert

  o Se ejecuta sobre la tabla alumnos.
  
  o Se ejecuta antes de una operación de inserción.
  
  o Se almacena la leyenda 'se ingreso un registro'

● Trigger2 : trigger_check_nota_before_update
  o Se ejecuta sobre la tabla alumnos.
  
  o Se ejecuta antes de una operación de actualización.
  
  o Se ingresa la leyenda 'se modifico un regisstro'
  
Una vez creados los triggers escribe varias sentencias de inserción y actualización
sobre la tabla alumnos y verifica que los triggers se están ejecutando
correctamente.

 Schema SQL

- CREATE DATABASE test1;
- 
- USE test1;
- 
- CREATE TABLE alumnos(
- id int NOT NULL AUTO_INCREMENT PRIMARY KEY,
- nombre varchar(50) NOT NULL,
- apellido1 varchar(50) NOT NULL,
- apellido2 varchar(50) NOT NULL,
- nota float NOT NULL
);

--Creacion del trigger
- CREATE TABLE registros(
- registro varchar(100)
- );
- 
- DELIMITER //
- CREATE TRIGGER trigger_check_nota_before_insert BEFORE INSERT ON alumnos
- FOR EACH ROW BEGIN
- INSERT INTO registros(registro) VALUES ('se ingreso un registro');
- END//
- DELIMITER ;
- 
- DELIMITER //
- CREATE TRIGGER tg_check_nota_before_update BEFORE UPDATE ON alumnos
- FOR EACH ROW BEGIN
- INSERT INTO registros(registro) VALUES ('se modifico un registro');
- END//
- DELIMITER ;
- 
- INSERT INTO alumnos VALUES(1,'Ernesto','Gonzales','Uri',4.0);
- UPDATE alumnos set nombre='Lucas'

 Query SQL
 
- USE test1;
- Select * FROM alumnos;
- Select * FROM registros;
- ![imagen](https://user-images.githubusercontent.com/102439815/173208594-76409d79-55c1-43e7-b158-7257120e540a.png)
- ![imagen](https://user-images.githubusercontent.com/102439815/173208825-84353f02-48bf-4070-954e-19f63ab40039.png)





