+++
title = "Restricciones dentro de un modelo entidad-relación"
date = "2022-11-19T09:20:57-04:00"
author = "Henrry Bourgeot"
authorTwitter = "estudiandev" #do not include @
cover = ""
tags = ["modelo relacional", "base de datos", "sistemas", "relacion", "bd"]
keywords = ["modelo relacional", "base de datos", "sistemas", "relacion", "bd"]
categories = ["bases de datos", "universidad"]
description = "En bases de datos, encontrarás dos tipos de restricciones, las **restricciones inherentes** y las **restricciones semánticas**, estas se encuentran en el modelo ER, y podrás ver lo que son en este breve post."
color = "blue" #color from the theme settings
+++

En bases de datos, encontrarás dos tipos de restricciones, las **restricciones inherentes** y las **restricciones semánticas**, estas se encuentran en el modelo ER, y podrás ver lo que son en este breve post.

## Restricciones inherentes al modelo

Estas son propias del modelo e indican las características propias de una relación, por tanto han de cumplirse obligatoriamente los siguientes puntos:

1. Ausencia de tuplas repetidas.
2. Irrelevancia del orden de las tuplas y atributos.
3. Cada atributo únicamente puede tomar un único valor del dominio al que pertenece.

## Restricciones Semánticas

1. **Restricción de Clave Primaria (PRIMARY KEY)**, permite declarar un atributo o conjunto de atributos como la clave primaria de una relación.
2. **Restricción de Unicidad (UNIQUE)**, permite que una clave alternativa o secundaria pueda tomar valores únicos para las tuplas de una relación (como si de una clave primaria se tratara). Se entiende que la clave primaria siempre tiene esta restricción.
3. **Restricción de Obligatoriedad (NOT NULL)**, permite declarar si uno o varios atributos de una relación debe tomar siempre un valor.
4. **Restricción de Integridad Referencial o de Clave Foránea (FOREIGN KEY)**, se utiliza para que mediante claves foráneas podamos enlazar relaciones de una base de datos. Además, nos indica que si una relación tiene una clave foránea que referencia a otra relación, cada valor de la clave foránea o ajena tiene que ser igual a un valor de la clave principal de la relación a la que referencia, o bien, ser completamente nulo. El diseñador de la base de datos deberá poder especificar qué operaciones han de rechazarse y cuáles han de aceptarse, y en este caso, qué operaciones de compensación hay que realizar para mantener la integridad de la base de datos. Para ello el diseñador debe plantearse tres preguntas por cada clave foránea:
   1. **¿Puede aceptar nulos esa clave foránea?** Por ejemplo, (tomando como referencia las relaciones PROVEEDORES, ARTICULOS) ¿tiene sentido la existencia de un articulo cuyo proveedor se desconoce? Evidentemente, no. En algunos casos esta respuesta podría ser distinta, por ejemplo, en una base de datos con las relaciones EMPLEADOS y DEPARTAMENTOS, podría existir un empleado no asignado de momento a un departamento.
   2. **¿Qué deberá suceder si se intenta eliminar una tupla referenciada por una clave foránea?** Por ejemplo, si se intenta eliminar un proveedor del cual existe algún artículo. En general, para estos casos existen por lo menos tres posibilidades:
      1. **Restringir**: La operación de eliminación se restringe sólo al caso en el que no existe alguna tupla con clave foránea que la referencie, rechazándose en caso contrario. En nuestro ejemplo, un proveedor podrá ser borrado, si y sólo si, por ahora, no suministra artículos.
      2. **Propagar en cascada**: La operación de borrado se propaga en cascada eliminando también todas las tuplas cuya clave foránea la referencien. En nuestro ejemplo, se eliminaría el proveedor y todas las tuplas de artículos suministrados por él.
      3. **Anular**: Se asignan nulos en la clave foránea de todas las tuplas que la referencien y se elimina la tupla referenciada. En nuestro ejemplo, no tiene mucho sentido, pero consistiría en asignar nulos al NIF-PROV de todas las tuplas de articulos pertenecientes al proveedor que queremos borrar, y posteriormente borrar al proveedor.
   3. **¿Qué deberá suceder si hay un intento de modificar la clave primaria de una tupla referenciada por una clave foránea?** Por ejemplo, si se intenta modificar la clave de un proveedor del cual existe algún artículo. Se actua con las mismas tres posibilidades que en el caso anterior:
      - Restringir
      - Propagar en cascada.
      - Anular
5. **Restricción de Valor por Defecto (DEFAULT)**, permite que cuando se inserte una tupla o registro en una tabla, para aquellos atributos para los cuales no se indique un valor exacto se les asigne un valor por defecto.
6. **Restricción de Verificación o Chequeo (CHECK)**, en algunos casos puede ocurrir que sea necesario especificar una condición que deben cumplir los valores de determinados atributos de una relación de la BD, aparte de las restricciones vistas anteriormente.
7. **Aserciones (ASSERTION)**: Esta restricción generaliza a la anterior, lo forman las aserciones en las que la condición se establece sobre elementos de distintas relaciones (por ello debe tener un nombre que la identifique).
8. **Disparadores (TRIGGERS)**, a veces puede interesar espeficar una acción distinta del rechazo cuando no se cumple una determinada restricción semántica. En este caso, se recurre al uso de disparadores o triggers que nos permiten además de indicar una condición, especificar la acción que queremos que se lleve a cabo si la condición se hace verdadera. Los disparadores pueden interpretarse como reglas del tipo evento-condición-acción (ECA) que pueden interpretarse como reglas que especifican que cuando se produce un evento, si se cumple una condición, entonces se realiza una determinada acción.
