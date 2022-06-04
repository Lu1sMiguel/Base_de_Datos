En la BD utilizada en clase realiza las siguientes consultas:

* La tabla empleado
* SELECT * FROM empleados
* ![imagen](https://user-images.githubusercontent.com/102439815/172027496-0b662ca7-62c4-4bff-b04b-f5a2e4e7977a.png)
* Los titulos de las revistas
* SELECT titulo FROM revista
* ![imagen](https://user-images.githubusercontent.com/102439815/172027886-47956092-49e5-4a71-be0b-123d6ca42ee7.png)
* Los nombres, apellidos y especialidad de los periodostas
* SELECT nombre_periodista, apellidos_periodista, especialidad FROM periodistas
* ![imagen](https://user-images.githubusercontent.com/102439815/172027976-94b21018-3223-4f5f-8795-17c3695ae869.png)
* Muestra los empleados que estan en x sucursal
* SELECT nombre_empleado, codigo_de_sucursal FROM empleados INNER JOIN sucursal on codigo_de_sucursal=nif;
* ![imagen](https://user-images.githubusercontent.com/102439815/172028518-c90b880a-2b45-4bf5-902e-3db83e819489.png)
* Muestra que periodistas colaboraron en x revista y en que sucursal se publico la revista
* Mustra que seccion esta en x revista, en que sucursal se imprimio y que empleados estan en esa sucursal.
* En la tabla peridistas muestra solo los que escriban sobre cine
* De la tabla revistas muestra las que sean de publicacion quincenal
* Muestra el nombre de ka revista que se hayan impreso despues del 30 de septiembre del 2021
* Muestra el nombre de la revista que se haya publicado en la sucursal 1 cuyos ejemplares tengan más de 80 páginas.

https://www.db-fiddle.com/f/iAUjGLoFoHtam2pK68Xh1B/1

