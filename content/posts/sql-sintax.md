+++
title = "Sintaxis de SQL"
date = "2022-11-04T16:58:42-04:00"
author = "Henrry Bourgeot"
authorTwitter = "estudiandev" #do not include @
tags = ["universidad", "sql", "programacion"]
categories = ["bases de datos", "universidad"]
keywords = ["universidad", "programacion", "base de datos", "sql", "estudiandev"]
description = "En esta página aprenderás lo necesario sobre la sintaxis del lenguaje de consultas estructurado (SQL), comandos, cláusulas, operadores..."
color = "orange" #color from the theme settings
+++

En el post [**Introducción a las Bases de Datos**](/introduccion-a-las-bases-de-datos) te hablé sobre lo que necesitas saber antes de aprender a fondo sobre estas, pero no sobre el lenguaje de consultas estructurado, en inglés: _Structured Query Language_, o por sus siglas globalmente como **SQL**. Aquí, aprenderás la sintaxis de este lenguaje, los comandos, cláusulas, operadores, y más de los que tiene este lenguaje. Pronto podrás ver posts sobre cómo crear bases de datos en sistemas gestores como MariaDB y PostgreSQL.

## ¿Qué es el Lenguaje de Consultas Estructurado (SQL)?

Te explicaré como me encantaría que me dijeran, es utilizado para administrar bases de datos **relacionales** y hacer varias operaciones con los datos que contienen estas o que se quieren manipular. No te voy a llenar de teoría como _cuándo fue creado_, lo importante de aquí es que sepas **para qué sirve este lenguaje**.

Este lenguaje se utiliza para modificar las tablas de las bases de datos que sean **relacionales** (las **no relacionales** NO usan este lenguaje), las operaciones que se realizan con este lenguaje se resumen en el acrónimo CRUD que observarás con mayor detenimiento más adelante. Si quieres aprender más teoría para un trabajo de investigación o algún otra tarea que tengas, te puede servir [este artículo](https://www.computerweekly.com/es/definicion/SQL-Structured-Query-Language-o-Lenguaje-de-consultas-estructuradas#:~:text=El%20lenguaje%20de%20consultas%20estructuradas,con%20los%20datos%20que%20contienen.) escrito por Jessica Sirkin de [ComputerWeekly.es](https://computerweekly.com).

## Comandos SQL

SQL en su sintaxis tiene ciertos **comandos** que se dividen en dos tipos principales.

### Comandos DLL (_Data Definition Language_)

Estos comandos permiten crear y definir nuevas bases de datos, igual que campos e índices. De acuerdo a lo que dice [GeoTalleres](https://geotalleres.readthedocs.io/es/latest/conceptos-sql/conceptos_sql.html), el lenguaje de definición de datos es el encargado de la modificación de la estructura de los objetos de la base de datos. Los comandos DLL son:

- **CREATE**: crea nuevas bases de datos, tablas, campos, vistas e índices.
- **DROP**: elimina tablas, bases de datos e índices, se DEBE usar con cuidado ya que la eliminación de estos datos **NO SE PUEDE REHACER**. Se debe diferenciar del comando _DELETE_.
- **ALTER**: este comando nos ayuda a modificar las tablas pudiendo agregar campos, eliminar campos, y también la definición de los campos.
- **TRUNCATE**: trunca todo el contenido de una tabla.

### Comandos DML

Estos a diferencia de los _comandos DLL_, permiten generar consultas para ordenar, filtrar y también extraer datos de la base de datos.

- **SELECT**: ayuda a consultar registros de la BD que satisfagan un criterio determinado.
- **INSERT**: carga los datos en una tabla definida en una sola operación.
- **UPDATE**: modifica los valores de los campos y registros especificados.
- **DELETE**: elimina registros de una tabla de una base de datos, al igual que el comando _drop_, no se pueden recuperar los registros borrados.

## Cláusulas

El lenguaje SQL también tiene cláusulas que son **condiciones de modificación que son normalmente utilizadas para definir los datos que se desean manipular o seleccionar**.

### _FROM_

Este comando especifica la tabla de la cual se van a seleccionar los registros.

### _WHERE_

Este detalla las condiciones que deben reunir los registros que van a ser seleccionados.

### _GROUP BY_

Separa los registros seleccionados en grupos específicos

### _HAVING_

Comando que detalla la condición que debe satisfacer cada grupo.

### _ORDER BY_

Este comando ordena los registros seleccionados de acuerdo a un orden que es determinado al realizar la consulta.

## Operadores

En el lenguaje de consultas estructurado existen **dos tipos de operadores**, los lógicos y de comparación.

### Operadores lógicos

- _AND_: literalmente, es el "y" lógico. Este operador evalúa dos condiciones y devuelve `true` únicamente si ambas son ciertas.
- _OR_: es el "o" lógico. A diferencia del comando anterior, evalúa dos condiciones y devuelve `true` si al menos una de las dos condiciones es cierta.
- _NOT_: es la negación lógica, ya que devuelve el valor contrario de la expresión.

### Operadores de Comparación

| Operador | Definición                                |
| -------- | ----------------------------------------- |
| <        | Menor que                                 |
| >        | Mayor que                                 |
| <>       | Distinto de                               |
| <=       | Menor o igual que                         |
| >=       | Mayor o igual que                         |
| BETWEEN  | Especifica un intervalo de valores        |
| LIKE     | Comparación de un modelo                  |
| IN       | Especifica registros de una base de datos |

## Funciones de agregado

Estas funciones son utilizadas dentro del comando _SELECT_ para luego devolver un único valor que se aplica a un grupo de registros determinados. Las funciones de agregado más usadas son:

- ### _AVG_
  Calcula el promedio de los valores de un campo específico.
- ### _COUNT_
  Esta función devuelve el número de registros de la selección.
- ### _SUM_
  Realiza la misma función que _AVG_, solo que en vez de calcular el promedio, devuelve la suma.
- ### _MAX_ y _MIN_
  Devuelven el valor más alto y bajo, respectivamente, de un campo especificado.

Por otro lado, SQL contiene varios **tipos de consultas**, tales como:

## Consultas de selección

Son utilizadas para indicar al motor de datos que devuelva información de las tablas, que es devuelta en forma de conjunto de registros que se pueden almacenar en un objeto, es importante mencionar que son modificables. La sintaxis básica de una consulta de selección es la siguiente:

```sql
SELECT campos FROM tabla;
```

Aunque estas consultas, pueden tener los siguientes predicados:

1. ALL: selecciona todos los campos y registros de una tabla, se denota con el asterisco.

```sql
SELECT * FROM tabla;
```

2. TOP: devuelve un determinado número de registros de la tabla, desde el primer registro hasta al último que se desee.
3. DISTINCT: omite los registros cuyos campos seleccionados coincidan totalmente. Tiene una variante llamada DISTINCROW que omite los registros duplicados basándose además en todos los registros.

```sql
SELECT DISTINCT(campo) FROM tabla;
```

En siguientes posts, encontrarás más ejemplos de código donde se usan los comandos de SQL.
