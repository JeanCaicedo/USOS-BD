# USOS-BD

![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)

Apuntes y prácticas de SQL estudiando la base de datos **Northwind** con SQLiteStudio. El repo funciona como una chuleta personal de los comandos y cláusulas aprendidos siguiendo el curso de Dalto en YouTube.

Es un repositorio de **notas de aprendizaje**, no un proyecto ejecutable. El valor está en el material pedagógico.

## Recursos

- Curso base: [Dalto — Curso de SQL](https://www.youtube.com/watch?v=DFg1V-rO6Pg)
- Base de datos: Northwind (incluida como proyecto `.sqbpro` para SQLiteStudio)

## Cómo abrirlo

1. Instalar [SQLiteStudio](https://sqlitestudio.pl/).
2. Abrir el archivo `Northwind.sqbpro`.
3. Ejecutar las consultas de ejemplo sobre las tablas de Northwind.

---

## Apuntes de SQL

### Comandos DDL (definir la estructura)

Definiendo cómo se almacena la información.

```sql
CREATE DATABASE nombre_bd;   -- crea una nueva base de datos vacía
DROP DATABASE nombre_bd;     -- elimina completamente una base de datos
CREATE TABLE nombre_tabla;   -- crea una tabla donde se almacena la información
ALTER TABLE nombre_tabla;    -- modifica una tabla existente
DROP TABLE nombre_tabla;     -- elimina por completo una tabla existente
```

### Comandos DML (manipular los datos)

```sql
SELECT   -- leer o seleccionar datos
INSERT   -- añadir nuevos datos
UPDATE   -- cambiar datos existentes
DELETE   -- eliminar datos existentes
REPLACE  -- añadir o cambiar datos nuevos o existentes
TRUNCATE -- vaciar todos los datos de una tabla
SET      -- establecer cambios
LIMIT    -- limitar el número de resultados
```

### Cláusula WHERE

Restringe el número de filas afectadas por una consulta `SELECT`, `UPDATE` o `DELETE`. Se puede combinar con operadores lógicos (`AND`, `OR`) y operadores de comparación (`=`, `!=`, `<`, `>`, etc.).

```sql
SELECT * FROM Customers
WHERE Country = 'Germany' AND City = 'Berlin';
```

### DISTINCT vs NOT (!=)

- `DISTINCT`: devuelve valores únicos, sin duplicados.
- `!=` / `NOT`: excluye los registros que cumplen una condición.

### Operadores lógicos

```sql
-- OR: el resultado es verdadero si alguna expresión es verdadera
SELECT * FROM Products WHERE CategoryID = 1 OR CategoryID = 2;

-- AND: el resultado es verdadero si ambas expresiones son verdaderas
SELECT * FROM Orders WHERE CustomerID = 'ALFKI' AND ShipCountry = 'Germany';

-- NOT: filtra registros negando una condición
SELECT * FROM Employees WHERE NOT Country = 'USA';
```

Los operadores lógicos se pueden combinar para construir consultas más específicas.

### Operador BETWEEN

Se usa para comparar dentro de un rango.

```sql
SELECT * FROM Products
WHERE Price BETWEEN 20 AND 30;
```

---

## Notas

- Material de estudio, con el nivel de detalle de quien está aprendiendo.
- Se conservan los apuntes originales como referencia personal.

## Autor

Jean Caicedo — [@JeanCaicedo](https://github.com/JeanCaicedo)
