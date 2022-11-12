+++
title = "Ejercicio de Bases de Datos"
date = "2022-11-11T20:55:19-04:00"
author = "Henrry Bourgeot"
authorTwitter = "estudiandev" #do not include @
cover = "img/ejercicio-sql.png"
tags = ["bases de datos", "universidad", "programacion", "mysql"]
keywords = ["bases de datos", "universidad", "programacion", "mysql", "workbench", "mysql workbench"]
description = "Seguramente, tienes la curiosidad de cómo un profesor puede plantear un ejercicio de una base de datos, la inserción, actualización, eliminación y consulta de datos, con el ejercicio que verás aquí, lograrás practicar paso a paso lo que veas"
color = "blue" #color from the theme settings
+++

Seguramente, tienes la curiosidad de cómo un profesor puede plantear un ejercicio de una base de datos, la inserción, actualización, eliminación y consulta de datos, con el ejercicio que verás a continuación, lograrás practicar paso a paso lo que veas en este post.

## Requisitos previos

Antes de empezar, debes tener:

1. Instalado MySQL/MariaDB server.
2. Instalado MySQL Workbench (por múltiples razones que explicaré más adelante).
3. Suficiente tiempo para realizar este ejercicio con calma.
4. Ganas de aprender.

## Enunciado

Para el presente ejercicio, deberás:

1. Crear una base de datos con el nombre `concesionario`.
2. Crear una tabla llamada `autos` con los siguientes campos:
   1. `matricula` (campo primario).
   2. `marca`.
   3. `modelo`.
   4. `color`.
   5. `kilometraje`.
3. Crear una tabla llamada `clientes` con los siguientes campos:
   1. `id_cliente` (campo primario).
   2. `nombre`.
   3. `domicilio`.
   4. `telefono`.
4. Insertar **3 registros** en cada una de las tablas.
5. Realizar las siguientes consultas:
   1. Mostrar solo el campo `marca` de todos los registros de los autos.
   2. Mostrar solo el campo `marca` de todos los registros de los autos omitiendo repetidos.
   3. Mostrar el `telefono` de todos los clientes que se llamen _"Juan"_
   4. Mostrar la `matricula` de los autos cuyo `modelo` sea _"Focus"_ y su `kilometraje` sea mayor que 50.000 (cincuenta mil).
   5. Mostrar el `kilometraje` de los autos cuya `marca` sea _"FORD", "RENAULT" O "FIAT"_.
   6. Mostrar **todos los campos** de los autos cuyo `kilometraje` esté entre 10.000 (diez mil) y 20.000 (veinte mil).
   7. Mostrar **todos los campos** de los autos cuyo `modelo` comience con _"GOL"_.
   8. Mostrar el **promedio de los `kilometraje`** de todos los autos.
   9. Mostrar todas las `marcas` de autos con su **promedio de `kilometraje`** y que estén agrupados por `marca`, siempre y cuando el **promedio de kilometraje** sea menor que 50.000 (cincuenta mil).
   10. Mostrar el **total** de los autos, el **nombre de la columna** será _"Total de Autos"_.

No sé si te habrás dado cuenta, pero dí algunas pistas para la resolución de los ejercicios, puedes comprobar la sintaxis en [este post](/sintaxis-de-sql).

## Resolución del enunciado

Vamos a resolver paso por paso el enunciado, primero creas la base de datos, y creas las tablas, de esta forma cumplimos los pasos 1 al 3:

```sql
CREATE DATABASE concesionario; -- creamos la BD

USE concesionario; -- la marcamos como actual


CREATE TABLE autos( -- creamos la tabla autos
  matricula VARCHAR(10) NOT NULL PRIMARY KEY, -- llave primaria
  marca VARCHAR(20) NOT NULL,
  modelo VARCHAR(30) NOT NULL,
  color VARCHAR(16) NOT NULL,
  kilometraje DOUBLE NOT NULL
);

CREATE TABLE clientes( -- creamos la tabla clientes
  id_cliente INT NOT NULL PRIMARY KEY AUTO_INCREMENT, -- llave primaria
  nombre VARCHAR(100) NOT NULL,
  domicilio TEXT NOT NULL,
  telefono VARCHAR(22) NOT NULL,
  matricula_auto VARCHAR(10) NOT NULL,
  FOREIGN KEY (matricula_auto) REFERENCES autos(matricula) ON DELETE CASCADE ON UPDATE CASCADE -- asignamos llave foránea y acciones
);
```

Con ello creado, te digo que **tú eres el que debe insertar los datos**, tienes que leer con detenimiento los datos que te dice el enunciado para insertarlos.

**TIP**: algunos de los datos los he descrito con paréntesis, y otros están en cursiva y entre comillas.

Ahora que sabes los tips para insetar, pasaré la sintaxis de la consultas que debes realizar:

### Consulta 5.1

```sql
SELECT marca FROM autos;
```

### Consulta 5.2

```sql
SELECT DISTINCT(marca) FROM autos;
```

### Consulta 5.3

```sql
SELECT telefono FROM clientes WHERE nombre = "juan";
```

### Consulta 5.4

```sql
SELECT matricula FROM autos WHERE modelo = "focus" AND kilometraje > 50;
```

### Consulta 5.5

```sql
SELECT kilometraje FROM autos WHERE marca = "Ford" OR marca = "Fiat" OR marca = "Renault";
```

### Consulta 5.6

```sql
SELECT * FROM autos WHERE kilometraje BETWEEN 10000 AND 20000;
```

### Consulta 5.7

```sql
SELECT * FROM autos WHERE modelo LIKE "gol%";
```

### Consulta 5.8

```sql
SELECT AVG(kilometraje) FROM autos;
```

### Consulta 5.9

```sql
SELECT marca, AVG(kilometraje) AS "kilometraje1" FROM autos GROUP BY marca HAVING AVG(kilometraje) < 50000 ORDER BY AVG(kilometraje) DESC;
```

### Consulta 5.10

```sql
SELECT COUNT(*) AS "TOTAL DE AUTOS" FROM autos;
```

Puedes encontrar ejemplos de estas consultas en [este post](/sintaxis-de-sql)
