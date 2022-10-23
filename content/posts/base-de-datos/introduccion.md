---
title: 'Introducción a la Base de Datos'
date: 2022-10-21T20:29:46-04:00
draft: false
categories: [base de datos, universidad, programación]
tags: [base de datos, universidad, sql, programas]
---

Seguramente, habrás escuchado acerca de las bases de datos, pero muchas veces uno no tiene una buena introducción a estas, por esto mismo en mi asignatura **Base de Datos** nos dieron una introducción a estas, y quiero compartirte los conocimientos que he adquirido con estos. Primero debes saber que existen varios tipos de bases de datos, las más usadas son las relacionales, que usan el Lenguaje de Consultas Estructurado, conocido como SQL por sus siglas en inglés (_Structured Query Language_), aunque hay otras bases de datos que son NoSQL, como MongoDB que es un _Sistema Gestor_ (lo verás más adelante) _de Base de Datos_ orientado a documentos, la sintaxis de estos documentos es muy parecida a un JSON (JavaScript Object Notation), por ello es usado MongoDB en los stacks fullstack de JavaScript (como MERN o MEAN).

## Pero en sí, ¿Qué son las Bases de Datos?

Podemos definirlas como una colección de datos, en que estos mismos son organizados para que se relacionen entre estos mismos. Si te parece muy vaga esta definición desde mi punto de vista, en [JavatPoint](https://www.javatpoint.com/what-is-database) definen una base de datos como una colección organizada de datos, a la que puede ser accedida y administrada con mucha facilidad.

Las bases de Datos tienen varios elementos de las que están compuestas, hablando de las **Bases de Datos relacionales**, constan de los siguientes:

1. Tablas: las tablas son entidades que contienen datos de un objeto en específico, estos pueden ser, por ejemplo, Autos, Clientes, Productos, Envíos, Útiles escolares, entre otros, un ejemplo digno de una tabla, es la matrícula de alumnos de una asignatura.
2. Campos: las tablas poseen campos, en los que se suministran los datos específicos que son requeridos, por ejemplo, un cliente puede tener como campos su nombre, apellido, dirección, teléfono y cédula de identidad (en otros países es conocido como DNI). Son las columnas de las tablas.
3. Registros: son los datos suministrados al realizar la inserción sobre esta tabla, por ejemplo, cada alumno que está matriculado en la asignatura _Corte y Costura_. Son las filas de una tabla.

Si esto no te quedó muy claro, tengo una representación gráfica que he realizado:

![Tabla de Base de Datos](/img/tabla-bd.png)

## Ventajas y Desventajas de las Bases de Datos.

Como ventajas, existen varias, que están relacionadas (en mayor parte) con los datos.

- Los datos son **coherentes** y **consistentes** porque se realiza un exhausto **control de redundancia** sobre estos, para así analizar y comprobar que los datos sean correctos y que no estén duplicados en la misma tabla.
- En cuanto a usuarios se refiere, existe una gran **flexibilidad** debido a que se pueden definir diversos roles dependiendo del uso que quiera desempeñar un usuario en específico. Por ejemplo, los usuarios utilizados por los programas que manejan bases de datos usualmente deben manejar la **inserción, lectura, modificación y eliminación** de datos.
- Los resultados, al igual que los datos, son **coherentes** por el previo control de redundancia anteriormente mencionado, sin embargo, como se aplica la **_normalización de documentos_**, logran aportar un **mayor valor informativo**.
- Cabe destacar que tienen en general, una gran **seguridad para proteger los datos**, cuentan con varios métodos de encriptación por defecto, aunque el programador puede también usar uno en el lenguaje de programación que se utilice en cierto programa.

Como desventajas, existen varias que tienen una gran importancia que se debe tener en cuenta:

- Los **gastos son altos**, la instalación es costosa y es necesario capacitar (o despedir) al personal para que desempeñen con buenas prácticas su rol como administrador de base de datos, aunque también es posible que tengan un rol como desarrolador, analista o diseñador (los veremos más adelante).
- Su implantación es **larga y difícil**.
- **No son rentables a corto plazo**, es decir, no verás resultados de gran relevancia en dos días, si no, al mes o incluso al año de contratar un servidor óptimo que aloje una base de datos que soporte una determinada cantidad de operaciones concurrentes.
