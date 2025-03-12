---
title: PostgreSQL
---

PostgreSQL es un sistema de gestión de bases de datos relacionales de código abierto, robusto y 
extensible, conocido por su soporte a SQL avanzado, transacciones y tipos de datos personalizados. 
Es ideal para aplicaciones que requieren fiabilidad y escalabilidad. Esta es una referencia rápida 
con los comandos y estructuras más esenciales de PostgreSQL, organizada por categorías.

---

## Configuración y básicos

| Comando/Concepto          | Descripción                                         |
|---------------------------|-----------------------------------------------------|
| `psql -U usuario -d base` | Conecta a una base de datos desde la terminal.      |
| `\l`                      | Lista todas las bases de datos (en psql).           |
| `\c nombre_base`          | Cambia a una base de datos específica (en psql).    |
| `\dt`                     | Lista todas las tablas de la base actual (en psql). |
| `-- Comentario`           | Comentario de una línea.                            |
| `/* Comentario */`        | Comentario multilínea.                              |
| `SELECT version();`       | Muestra la versión de PostgreSQL instalada.         |

---

## Creación y gestión de bases de datos

| Comando                                         | Descripción                                    |
|-------------------------------------------------|------------------------------------------------|
| `CREATE DATABASE nombre;`                       | Crea una nueva base de datos.                  |
| `DROP DATABASE nombre;`                         | Elimina una base de datos existente.           |
| `ALTER DATABASE nombre RENAME TO nuevo_nombre;` | Renombra una base de datos.                    |
| `SELECT datname FROM pg_database;`              | Lista todas las bases de datos en el servidor. |

---

## Creación y gestión de tablas

| Comando                                             | Descripción                                |
|-----------------------------------------------------|--------------------------------------------|
| `CREATE TABLE nombre (col tipo);`                   | Crea una tabla con columnas especificadas. |
| `DROP TABLE nombre;`                                | Elimina una tabla existente.               |
| `ALTER TABLE nombre ADD COLUMN col tipo;`           | Añade una nueva columna a la tabla.        |
| `ALTER TABLE nombre DROP COLUMN col;`               | Elimina una columna de la tabla.           |
| `SELECT table_name FROM information_schema.tables;` | Lista tablas de la base actual.            |

---

## Tipos de datos comunes

| Tipo             | Descripción                                                    |
|------------------|----------------------------------------------------------------|
| `INTEGER`        | Entero (4 bytes).                                              |
| `VARCHAR(n)`     | Texto de longitud variable (máx. `n` caracteres).              |
| `TEXT`           | Texto de longitud ilimitada.                                   |
| `TIMESTAMP`      | Fecha y hora con zona horaria opcional.                        |
| `NUMERIC(p,s)`   | Número decimal con `p` dígitos totales y `s` decimales.        |
| `BOOLEAN`        | Valor booleano (`true` o `false`).                             |
| `JSON` / `JSONB` | Almacena datos en formato JSON (JSONB es binario, más rápido). |

---

## Consultas básicas (SELECT)

| Comando                           | Descripción                                   |
|-----------------------------------|-----------------------------------------------|
| `SELECT col1, col2 FROM tabla;`   | Selecciona columnas específicas de una tabla. |
| `SELECT * FROM tabla;`            | Selecciona todas las columnas de una tabla.   |
| `SELECT DISTINCT col FROM tabla;` | Elimina duplicados en los resultados.         |
| `SELECT col FROM tabla LIMIT n;`  | Limita a los primeros `n` registros.          |
| `SELECT col AS alias FROM tabla;` | Asigna un alias a una columna.                |

---

## Filtrado y ordenamiento

| Comando                      | Descripción                                               |
|------------------------------|-----------------------------------------------------------|
| `WHERE col = valor;`         | Filtra registros según una condición.                     |
| `WHERE col BETWEEN a AND b;` | Filtra en un rango de valores.                            |
| `WHERE col IN (val1, val2);` | Filtra por valores específicos.                           |
| `WHERE col LIKE '%texto%';`  | Busca coincidencias de patrones (% = cualquier carácter). |
| `ORDER BY col ASC/DESC;`     | Ordena resultados ascendente o descendente.               |

---

## Inserción, actualización y eliminación

| Comando                                               | Descripción                                   |
|-------------------------------------------------------|-----------------------------------------------|
| `INSERT INTO tabla (col1, col2) VALUES (val1, val2);` | Inserta un nuevo registro.                    |
| `UPDATE tabla SET col = val WHERE condicion;`         | Actualiza registros según una condición.      |
| `DELETE FROM tabla WHERE condicion;`                  | Elimina registros según una condición.        |
| `TRUNCATE TABLE tabla;`                               | Elimina todos los datos de la tabla (rápido). |

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

| Comando                                       | Descripción                                           |
|-----------------------------------------------|-------------------------------------------------------|
| `INNER JOIN tabla2 ON t1.col = t2.col;`       | Une tablas, solo coincidencias.                       |
| `LEFT OUTER JOIN tabla2 ON t1.col = t2.col;`  | Incluye todos de `t1`, nulos si no hay match en `t2`. |
| `RIGHT OUTER JOIN tabla2 ON t1.col = t2.col;` | Incluye todos de `t2`, nulos si no hay match en `t1`. |
| `FULL OUTER JOIN tabla2 ON t1.col = t2.col;`  | Incluye todos los registros de ambas tablas.          |

---

## Índices y claves

| Comando                                    | Descripción                                 |
|--------------------------------------------|---------------------------------------------|
| `CREATE INDEX idx_nombre ON tabla(col);`   | Crea un índice para acelerar consultas.     |
| `DROP INDEX idx_nombre;`                   | Elimina un índice existente.                |
| `PRIMARY KEY`                              | Define una clave primaria (única, no nula). |
| `FOREIGN KEY (col) REFERENCES tabla(col);` | Define una clave foránea para relaciones.   |

---

## Comandos avanzados: Vistas y funciones

| Comando                                                                | Descripción                            |
|------------------------------------------------------------------------|----------------------------------------|
| `CREATE VIEW nombre AS SELECT ...;`                                    | Crea una vista basada en una consulta. |
| `DROP VIEW nombre;`                                                    | Elimina una vista existente.           |
| `CREATE FUNCTION nombre() RETURNS tipo AS $$ ... $$ LANGUAGE plpgsql;` | Crea una función en PL/pgSQL.          |
| `SELECT nombre();`                                                     | Ejecuta una función definida.          |

---

## Comandos avanzados: Transacciones

| Comando                         | Descripción                                            |
|---------------------------------|--------------------------------------------------------|
| `BEGIN;`                        | Inicia una transacción.                                |
| `COMMIT;`                       | Confirma los cambios de la transacción.                |
| `ROLLBACK;`                     | Deshace los cambios de la transacción.                 |
| `SAVEPOINT nombre;`             | Define un punto de guardado dentro de una transacción. |
| `ROLLBACK TO SAVEPOINT nombre;` | Revierte hasta un punto de guardado.                   |

---

## Comandos avanzados: Funciones de fecha

| Comando                     | Descripción                                         |
|-----------------------------|-----------------------------------------------------|
| `NOW()`                     | Devuelve la fecha y hora actuales.                  |
| `DATE_TRUNC('unit', fecha)` | Trunca una fecha a una unidad (ej. 'day', 'month'). |
| `EXTRACT(unit FROM fecha)`  | Extrae una parte de la fecha (ej. 'year', 'day').   |
| `fecha + INTERVAL 'n unit'` | Suma `n` unidades (ej. '1 day') a una fecha.        |

---

## Gestión de usuarios y permisos

| Comando                                          | Descripción                               |
|--------------------------------------------------|-------------------------------------------|
| `CREATE ROLE nombre WITH LOGIN PASSWORD 'pass';` | Crea un usuario con contraseña.           |
| `DROP ROLE nombre;`                              | Elimina un usuario.                       |
| `GRANT SELECT ON tabla TO usuario;`              | Otorga permisos específicos a un usuario. |
| `REVOKE SELECT ON tabla FROM usuario;`           | Revoca permisos a un usuario.             |
| `ALTER ROLE nombre SET search_path TO esquema;`  | Configura el esquema por defecto.         |

---

## Comandos avanzados: Características específicas

| Comando                                     | Descripción                                   |
|---------------------------------------------|-----------------------------------------------|
| `COPY tabla FROM 'ruta.csv' DELIMITER ',';` | Importa datos desde un archivo CSV.           |
| `COPY tabla TO 'ruta.csv' DELIMITER ',';`   | Exporta datos a un archivo CSV.               |
| `CREATE TABLE nombre (col SERIAL);`         | Columna autoincremental (secuencia).          |
| `SELECT json_agg(col) FROM tabla;`          | Agrega datos en formato JSON.                 |
| `EXPLAIN SELECT ...;`                       | Muestra el plan de ejecución de una consulta. |
