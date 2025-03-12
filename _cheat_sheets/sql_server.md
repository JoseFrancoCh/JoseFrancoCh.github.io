---
title: SQL Server
---

SQL Server es un sistema de gestión de bases de datos relacionales desarrollado por Microsoft, 
conocido por su integración con herramientas empresariales, rendimiento y soporte para grandes 
volúmenes de datos. Esta es una referencia rápida con los comandos y estructuras más esenciales 
de SQL Server, organizada por categorías.

---

## Configuración y básicos

| Comando/Concepto                      | Descripción                                 |
|---------------------------------------|---------------------------------------------|
| `SQL Server Management Studio (SSMS)` | Interfaz gráfica para gestionar SQL Server. |
| `SELECT @@VERSION`                    | Muestra la versión de SQL Server instalada. |
| `USE nombre_base`                     | Cambia a una base de datos específica.      |
| `GO`                                  | Delimita bloques de comandos en SSMS.       |
| `-- Comentario`                       | Comentario de una línea.                    |
| `/* Comentario */`                    | Comentario multilínea.                      |

---

## Creación y gestión de bases de datos

| Comando                                            | Descripción                                    |
|----------------------------------------------------|------------------------------------------------|
| `CREATE DATABASE nombre`                           | Crea una nueva base de datos.                  |
| `DROP DATABASE nombre`                             | Elimina una base de datos existente.           |
| `ALTER DATABASE nombre MODIFY NAME = nuevo_nombre` | Renombra una base de datos.                    |
| `SELECT * FROM sys.databases`                      | Lista todas las bases de datos en el servidor. |

---

## Creación y gestión de tablas

| Comando                                      | Descripción                                 |
|----------------------------------------------|---------------------------------------------|
| `CREATE TABLE nombre (col1 tipo, col2 tipo)` | Crea una tabla con columnas especificadas.  |
| `DROP TABLE nombre`                          | Elimina una tabla existente.                |
| `ALTER TABLE nombre ADD col tipo`            | Añade una nueva columna a la tabla.         |
| `ALTER TABLE nombre DROP COLUMN col`         | Elimina una columna de la tabla.            |
| `SELECT * FROM INFORMATION_SCHEMA.TABLES`    | Lista todas las tablas de la base de datos. |

---

## Tipos de datos comunes

| Tipo           | Descripción                                             |
|----------------|---------------------------------------------------------|
| `INT`          | Entero (4 bytes).                                       |
| `VARCHAR(n)`   | Texto de longitud variable (máx. `n` caracteres).       |
| `NVARCHAR(n)`  | Texto Unicode de longitud variable.                     |
| `DATETIME`     | Fecha y hora (precisión hasta 3.33 ms).                 |
| `DECIMAL(p,s)` | Número decimal con `p` dígitos totales y `s` decimales. |
| `BIT`          | Valor booleano (0 o 1).                                 |

---

## Consultas básicas (SELECT)

| Comando                          | Descripción                                   |
|----------------------------------|-----------------------------------------------|
| `SELECT col1, col2 FROM tabla`   | Selecciona columnas específicas de una tabla. |
| `SELECT * FROM tabla`            | Selecciona todas las columnas de una tabla.   |
| `SELECT DISTINCT col FROM tabla` | Elimina duplicados en los resultados.         |
| `SELECT TOP n col FROM tabla`    | Limita a los primeros `n` registros.          |
| `SELECT col AS alias FROM tabla` | Asigna un alias a una columna.                |

---

## Filtrado y ordenamiento

| Comando                     | Descripción                                               |
|-----------------------------|-----------------------------------------------------------|
| `WHERE col = valor`         | Filtra registros según una condición.                     |
| `WHERE col BETWEEN a AND b` | Filtra en un rango de valores.                            |
| `WHERE col IN (val1, val2)` | Filtra por valores específicos.                           |
| `WHERE col LIKE '%texto%'`  | Busca coincidencias de patrones (% = cualquier carácter). |
| `ORDER BY col ASC/DESC`     | Ordena resultados ascendente o descendente.               |

---

## Inserción, actualización y eliminación

| Comando                                              | Descripción                                                  |
|------------------------------------------------------|--------------------------------------------------------------|
| `INSERT INTO tabla (col1, col2) VALUES (val1, val2)` | Inserta un nuevo registro.                                   |
| `UPDATE tabla SET col = val WHERE condicion`         | Actualiza registros según una condición.                     |
| `DELETE FROM tabla WHERE condicion`                  | Elimina registros según una condición.                       |
| `TRUNCATE TABLE tabla`                               | Elimina todos los datos de la tabla (sin borrar estructura). |

---

## Agregación y funciones

| Comando                | Descripción                                  |
|------------------------|----------------------------------------------|
| `COUNT(col)`           | Cuenta registros no nulos.                   |
| `SUM(col)`             | Suma los valores de una columna numérica.    |
| `AVG(col)`             | Calcula el promedio de una columna numérica. |
| `MIN(col)`, `MAX(col)` | Obtiene el valor mínimo o máximo.            |
| `GROUP BY col`         | Agrupa resultados por una columna.           |
| `HAVING condicion`     | Filtra grupos después de `GROUP BY`.         |

---

## Joins (Uniones)

| Comando                                | Descripción                                           |
|----------------------------------------|-------------------------------------------------------|
| `INNER JOIN tabla2 ON t1.col = t2.col` | Une tablas, solo coincidencias.                       |
| `LEFT JOIN tabla2 ON t1.col = t2.col`  | Incluye todos de `t1`, nulos si no hay match en `t2`. |
| `RIGHT JOIN tabla2 ON t1.col = t2.col` | Incluye todos de `t2`, nulos si no hay match en `t1`. |
| `FULL JOIN tabla2 ON t1.col = t2.col`  | Incluye todos los registros de ambas tablas.          |

---

## Índices y claves

| Comando                                   | Descripción                                 |
|-------------------------------------------|---------------------------------------------|
| `CREATE INDEX idx_nombre ON tabla(col)`   | Crea un índice para acelerar consultas.     |
| `DROP INDEX idx_nombre ON tabla`          | Elimina un índice existente.                |
| `PRIMARY KEY`                             | Define una clave primaria (única, no nula). |
| `FOREIGN KEY (col) REFERENCES tabla(col)` | Define una clave foránea para relaciones.   |

---

## Comandos avanzados: Vistas y procedimientos

| Comando                                    | Descripción                            |
|--------------------------------------------|----------------------------------------|
| `CREATE VIEW nombre AS SELECT ...`         | Crea una vista basada en una consulta. |
| `DROP VIEW nombre`                         | Elimina una vista existente.           |
| `CREATE PROCEDURE nombre AS BEGIN ... END` | Crea un procedimiento almacenado.      |
| `EXEC nombre`                              | Ejecuta un procedimiento almacenado.   |

---

## Comandos avanzados: Transacciones

| Comando                  | Descripción                                            |
|--------------------------|--------------------------------------------------------|
| `BEGIN TRANSACTION`      | Inicia una transacción.                                |
| `COMMIT`                 | Confirma los cambios de la transacción.                |
| `ROLLBACK`               | Deshace los cambios de la transacción.                 |
| `SAVE TRANSACTION punto` | Define un punto de guardado dentro de una transacción. |

---

## Comandos avanzados: Funciones de fecha

| Comando                            | Descripción                                   |
|------------------------------------|-----------------------------------------------|
| `GETDATE()`                        | Devuelve la fecha y hora actuales.            |
| `DATEADD(unidad, n, fecha)`        | Suma `n` unidades (ej. día, mes) a una fecha. |
| `DATEDIFF(unidad, fecha1, fecha2)` | Diferencia en unidades entre dos fechas.      |
| `FORMAT(fecha, 'yyyy-MM-dd')`      | Formatea una fecha según un patrón.           |

---

## Gestión de usuarios y permisos

| Comando                                      | Descripción                               |
|----------------------------------------------|-------------------------------------------|
| `CREATE LOGIN nombre WITH PASSWORD = 'pass'` | Crea un inicio de sesión.                 |
| `CREATE USER nombre FOR LOGIN nombre`        | Crea un usuario asociado a un login.      |
| `GRANT SELECT ON tabla TO usuario`           | Otorga permisos específicos a un usuario. |
| `REVOKE SELECT ON tabla FROM usuario`        | Revoca permisos a un usuario.             |

