+++
title = "Sintaxis de SQL"
date = "2022-11-04T16:58:42-04:00"
author = "Henrry Bourgeot"
authorTwitter = "estudiandev" #do not include @
tags = ["universidad", "sql", "programacion"]
keywords = ["universidad", "programacion", "base de datos", "sql"]
description = ""
color = "orange" #color from the theme settings
+++

En el post [**Introducción a las Bases de Datos**](/introduccion-a-las-bases-de-datos) te hablé sobre lo que necesitas saber antes de aprender a fondo sobre estas, pero no sobre el lenguaje de consultas estructurado, en inglés: _Structured Query Language_, o por sus siglas globalmente como **SQL**. Aquí, aprenderás la sintaxis de este lenguaje, los comandos, cláusulas, operadores, y más de los que tiene este lenguaje. Pronto podrás ver posts sobre cómo crear bases de datos en sistemas gestores como MariaDB y PostgreSQL.

## ¿Qué es el Lenguaje de Consultas Estructurado (SQL)?

Te explicaré como me encantaría que me dijeran, es utilizado para administrar bases de datos **relacionales** y hacer varias operaciones con los datos que contienen estas o que se quieren manipular. No te voy a llenar de teoría como _cuándo fue creado_, lo importante de aquí es que sepas **para qué sirve este lenguaje**.

Este lenguaje se utiliza para modificar las tablas de las bases de datos que sean **relacionales** (las **no relacionales** NO usan este lenguaje), las operaciones que se realizan con este lenguaje se resumen en el acrónimo CRUD que observarás con mayor detenimiento más adelante. Si quieres aprender más teoría para un trabajo de investigación o algún otra tarea que tengas, te puede servir [este artículo](https://www.computerweekly.com/es/definicion/SQL-Structured-Query-Language-o-Lenguaje-de-consultas-estructuradas#:~:text=El%20lenguaje%20de%20consultas%20estructuradas,con%20los%20datos%20que%20contienen.) escrito por Jessica Sirkin de [ComputerWeekly.es](https://computerweekly.com).

## Comandos SQL

SQL en su sintaxis tiene ciertos **comandos** que se dividen en dos tipos principales.

### Comandos DLL

Estos comandos permiten crear y definir nuevas bases de datos, igual que campos e índices. Los comandos DLL son:

- **CREATE**: crea nuevas bases de datos, tablas, campos, vistas e índices.
- **DROP**: elimina tablas, bases de datos e índices, se DEBE usar con cuidado ya que la eliminación de estos datos **NO SE PUEDE REHACER**. Se debe diferenciar del comando _DELETE_.
- **ALTER**: este comando nos ayuda a modificar las tablas pudiendo agregar campos, eliminar campos, y también la definición de los campos.

### Comandos DML

Estos a diferencia de los _comandos DLL_, permiten generar consultas para ordenar, filtrar y también extraer datos de la base de datos.

- **SELECT**: ayuda a consultar registros de la BD que satisfagan un criterio determinado.
- **INSERT**: carga los datos en una tabla definida en una sola operación.
- **UPDATE**: modifica los valores de los campos y registros especificados.
- **DELETE**: elimina registros de una tabla de una base de datos, al igual que el comando _drop_, no se pueden recuperar los registros borrados.
