---
title: 'Introducción a la Base de Datos'
date: 2022-10-21T20:29:46-04:00
draft: false
author: 'Henrry Bourgeot'
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

## Tipos de Usuarios en las bases de datos

Existen varios tipos de usuarios en las bases de datos, estos poseen sus respectivos roles para evitar la pérdida de información almacenada en ellas. Principalmente, se dividen en dos, los usuarios finales y los usuarios informáticos.

### Usuarios informáticos

- **Diseñadores**: estos usuarios comprenden los requisitos relacionados con las bases de Datos, como:

  - Diseño.
  - Apariencia.
  - Funcionamiento.
  - Programación.
  - Costos.

  Cabe destacar que estos son la primer persona que se debe contactar cuando se requiere crear una base de datos, por otro lado, cuando ya han obtenido toda la información necesaria realizan el diseño correspondiente para después entregar este a los programadores la desarrollen en el sistema gestor.

- **Administradores de Bases de Datos**: tienen el control **total**, por esto mismo son comúnmente llamados como _superusuarios_. Un administrador se encarga de definir los esquemas lógicos y físicos, además de gestionar los tres niveles de las bases de datos: interno, conceptual y externo (si quieres conocer más sobre estos, te recomiendo [este enlace](https://daimaouds.wixsite.com/basededatosudoak/single-post/2015/06/21/arquitectura-de-base-de-datos-arquitectura-de-3-niveles#:~:text=Los%20tres%20niveles%20de%20la,%3A%20Interno%2C%20Conceptual%20y%20Externo)), por último, las funciones que realizan son:
  1. Conceden/revocan **permisos a todos los usuarios**.
  2. **Diseñan la estructura general**, esto incluye diseños, funcionamiento, procedimiento y motivos.
  3. Son **responsables del mantenimiento, respaldo y recuperación** de las bases de datos.
  4. Realizan todas las **actividades relacionadas con la administración**.
  5. Proporcionan soporte técnico.
- **Analistas**: ellos se encargan de verificar las opciones que sean similares y actuales, también hacen todo lo necesario para cambiar o actualizar el diseño final para que sean únicos. Además, se aseguran de que el comprador esté satisfecho con el producto.
- **Desarrolladores**: realizan la codificación y desarrollo para que el diseño final sea una entidad del mundo real.

### Usuarios Finales

Son los clientes que usan la base de datos para completar a través de consultas la información, aunque en su mayoría no saben cómo se utilizan las bases de datos, por esto mismo, para minimizar la posibilidad de que ocurran errores, su usuario debe estar limitado para que no exista la pérdida de información.

## ¿Qué es un Sistema Gestor de Base de Datos?

Es un conjunto de programas que permiten el desarrollo, acceso y mantenimiento de las bases de datos, seguramente conoces al menos uno de los que te nombraré a continuación:

1. MySQL.
2. Oracle.
3. MariaDB.
4. PostgreSQL.
5. SQL Server.

Existen otros más que no he mencionado aquí, pero los anteriores son los más usados, personalmente, me gusta PostgreSQL, tú pronto sabrás cuál es tu preferida cuando las uses ;).

### ¿Qué es un Sistema de Base de Datos?

Vulgarmente, son el **Sistema Gestor de BD** que contiene **datos** y posee **usuarios**. Aunque, literalmente, los sistemas gestores que mencioné anteriormente, son Sistemas de BD ya que albergan usuarios. Estos se componen de:

- La estructura Lógica del Usuario.
- La estructura lógica global.
- La estructura física.

### Operaciones

Con un Sistema de BD, podemos reslizar varias operaciones, en concreto, se pueden colocar las operaciones en una tabla.

| Sobre el conjunto de datos | Sobre registros específicos |
| -------------------------- | --------------------------- |
| Creación                   | Inserción                   |
| Restauración               | Eliminación                 |
| Consultas globales         | Modificación                |
|                            | Consultas con filtros       |

### Funciones

Estos también desarrollan ciertas funciones que son importantes:

1. Descripción o definición.
2. Manipulación.
3. Control.
4. Procedimientos para el administrador:
   - Transacciones.
   - Reorganización.
   - Copias de Seguridad.
   - Estadísticas.
   - Carga de ficheros.
