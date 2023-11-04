Seleccionando Columnas
```
SELECT * FROM nombre_tabla;
SELECT email FROM usuarios;
SELECT nombre, apellido, edad FROM nombre_tabla;
SELECT col1 AS col_nombre1 FROM tabla;
SELECT col1 AS col_nombre1, col2 AS col_nombre2 FROM tabla;
SELECT nombre_completo, sueldo AS "Salario de Empleados" FROM empleados;
```
Seleccionando filas
```
SELECT * FROM productos WHERE precio > 100;
SELECT * FROM productos WHERE precio >= 100;
SELECT * FROM productos WHERE col1 < 10;
SELECT id, nombre FROM productos WHERE precio > 30;
SELECT * FROM productos WHERE precio = 100;
SELECT * FROM productos WHERE nombre = 'Camiseta';
SELECT * FROM productos WHERE destacado = true;
SELECT * FROM usuarios WHERE status = false;
SELECT * FROM usuarios WHERE nombre = 'Juan' AND apellido = 'Pérez';
SELECT * FROM productos WHERE fecha_de_creación >= '2022-01-01';
SELECT * FROM productos WHERE stock BETWEEN 10 AND 50;
SELECT * FROM usuarios WHERE nombre LIKE 'J%'
SELECT * FROM empleados WHERE nombre IS NOT NULL;
```
Ordenando resultados (orden y limit)
```
SELECT * FROM productos ORDER BY precio;
SELECT * FROM productos ORDER BY precio ASC;
SELECT * FROM productos ORDER BY precio DESC;
Con NULLS FIRST se muestran los nulos primeros y con NULLS LAST se muestran al final:
SELECT * FROM tabla ORDER BY campo NULLS FIRST
SELECT * FROM productos ORDER BY stock ASC, color ASC
SELECT * FROM productos WHERE precio > 100 ORDER BY precio DESC, nombre ASC;
```
Limit
```
SELECT * FROM tabla LIMIT 5
SELECT * FROM tabla WHERE campo > 10 ORDER BY campo2 LIMIT 5
SELECT * FROM notas ORDER BY nota DESC LIMIT 3
```
Operaciones con strings
```
SELECT UPPER(nombre) FROM usuarios; - convertir a mayuscula
SELECT LOWER(nombre) AS nombre_minusculas FROM productos; convertir a minuscula
SELECT TRIM(nombre) FROM productos; - Quitando espacios en blanco
SELECT LOWER(TRIM(email)) as email_limpios from usuarios;
SELECT nombre, LENGTH(nombre) FROM usuarios; - Obtener el largo de un string
SELECT LENGTH(nombre) as largo_nombre FROM usuarios ORDER BY LENGTH(nombre) LIMIT 1 ;
SELECT email FROM usuarios ORDER BY LENGTH(email) DESC LIMIT 1; - Ordenando todos los datos y la función
SELECT nombre || ' ' || apellido AS nombre_completo FROM empleados;
SELECT SUBSTR(nombre, 1, 1) AS primera_letra FROM productos; - Seleccionando caracteres de un string
```
Operaciones con fechas
```
SELECT * FROM usuarios WHERE fecha_registro = DATE('now'); - Fecha de hoy
DATE('now', '1 day') - fecha de mañana
2 Semanas: DATE('now', '2 week') 3 Meses: DATE('now', '3 month')
DATE('now', '-1 day') DATE('now', '-1 week')
SELECT *, strftime('%Y', fecha_venta) as año_venta FROM ventas - extracción de año
SELECT strftime('%m', columna) FROM tabla - extracción de mes
strftime('%Y-%m') - extracción de año y mes
SELECT * FROM ventas WHERE strftime('%Y', fecha_venta) = '2012';
```
Funciones de agregación
```
SELECT MAX(columna) FROM tabla
SELECT MIN(columna) FROM tabla
SELECT SUM(columna) FROM tabla
SELECT AVG(columna) FROM tabla
SELECT COUNT(*) FROM tabla
SELECT AVG(columna1) FROM tabla WHERE columna2 < valor
```
Distinct
```
SELECT DISTINCT color AS color_unico FROM colores
SELECT DISTINCT strftime('%Y', fecha_venta) as año_unico FROM ventas
SELECT COUNT(DISTINCT Departamento) FROM Empleados;
select DISTINCT strftime('%m',fecha_venta) as mes_unico from ventas - Seleccionar distintos años
SELECT COUNT(DISTINCT Departamento) FROM Empleados;
select count (distinct telefono)  as telefonos_unicos from usuarios - contar valores distintos
SELECT DISTINCT departamento, puesto FROM empleados;
```
Introducción a grupos
```
SELECT color as color_unico FROM colores GROUP BY color
select correo, count (correo) as repeticiones from usuarios group by correo - agrupar y contar
select departamento, count(departamento) as cantidad_empleados from empleados group by departamento 
SELECT Cliente, SUM(Monto) AS Monto_Total FROM pedidos GROUP BY Cliente;
select categoria, sum(monto) as monto_total from ventas group by categoria
select  nombre_completo , avg(nota) as promedio_notas from estudiantes group by nombre_completo
select categoria, max(monto)as monto_mas_alto from ventas group by categoria
select categoria, min(monto) as monto_mas_bajo from ventas group by categoria
select  sum(monto)as suma_ventas, strftime ('%m',fecha_venta)as mes from ventas group by strftime ('%m',fecha_venta)
select correo,count (correo) as repeticiones from usuarios group by 1 order by 1
select correo, materia,avg(nota) as promedio_notas from estudiantes group by 1,2
```
Having
```
select strftime('%m',FECHA_INSCRIPCION) as mes, count (FECHA_INSCRIPCION) as cantidad_usuarios
from inscripciones
group by strftime('%m',FECHA_INSCRIPCION)
having cantidad_usuarios=1

select correo, count (correo) as cuenta_correos from correos_corporativos group by correo having cuenta_correos>1
select count(nombre) as cantidad_de_usuarios, departamento from empleados group by departamento having cantidad_de_usuarios>1
select email,avg (notas) as promedio_notas from notas group by email having promedio_notas >=50
```
El orden de las clausulas en una consulta debe ser el siguiente:
ORDEN	CLAUSULA	DESCRIPCIÓN
1	SELECT	Especifica las columnas que se deben retornar en el resultado.
2	FROM	Especifica las tablas de las cuales se extraerán los datos.
3	WHERE	Filtra registros antes de cualquier agregación o agrupación.
4	GROUP BY	Agrupa registros por una o más columnas.
5	HAVING	Filtra registros después de la agregación.
6	ORDER BY	Ordena los registros retornados por una o más columnas.
7	LIMIT	Limita el número de registros retornados.
```
Select producto,  sum (cantidad) as cantidad_total from ventas 
group by producto 
having cantidad_total >1000
order by cantidad_total desc

select  departamento, avg(salario) as salario_promedio from empleados 
group by departamento 
having salario_promedio >3000 
order by salario_promedio desc
```
Subconsultas
```

```
