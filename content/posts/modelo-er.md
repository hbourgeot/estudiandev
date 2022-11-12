+++
title = "Modelo Entidad Relación"
date = "2022-11-09T08:11:09-04:00"
author = "Henrry Bourgeot"
authorTwitter = "estudiandev" #do not include @
cover = ""
tags = ["programacion", "modelo er", "sql", "bases de datos"]
keywords = ["programacion", "sql"]
description = "Seguramente si estás comenzando a ver [bases de datos](/introduccion-a-las-bases-de-datos) lo más seguro es que hayas empezado (o comiences) a ver este tema, por lo que te recomiendo que leas este post completo para que puedas comprender lo que es el modelo ER."
color = "blue" #color from the theme settings
+++

Seguramente si estás comenzando a ver [bases de datos](/introduccion-a-las-bases-de-datos) lo más seguro es que hayas empezado (o comiences) a ver este tema, por lo que te recomiendo que leas este post completo para que puedas comprender lo que es el **modelo ER**.

## ¿Qué es un modelo entidad relación?

También conocido como diagrama entidad-relación, es un tipo de diagrama de flujo que explica cómo las _entidades_ (personas, objetos o incluso conceptos) se relacionan entre sí dentro de un sistema.

Ejemplificando, una tienda, tiene como _entidades_ a los **clientes, productos, empleados y personal directivo**, y una de las tantas _relaciones_ que pueden existir proveniendo de estas entidades, es la _**compra** de productos por parte del cliente_.

## Elementos

Todo modelo ER, consta de tres elementos fundamentales:

1. Entidades: hacen referencia a personas, objetos o conceptos.
2. Atributos: son aquellas características que posee una persona, objeto o concepto. Estos atributos pueden ser simples (no tienen derivados) o compuestos (tienen derivados).
3. Relaciones: se establecen vínculos entre parejas de entidades.

### Características de las Entidades:

1. Pueden ser identificados individualmente.
2. Desempeña un papel necesario en el sistema a ser desarrollado.
3. Puede ser descrito por uno o más elementos de datos.

## ¿Cómo se debe diseñar una base de datos?

El diseño de una base de datos es el proceso de formular el contenido de las tablas que almacenan los datos. Y existen unos pasos para poder realizar efectivamente el diseño de las bases de datos.

### Recolección y Análisis de requerimientos

Los datos deben ser obtenidos y además documentados mediante una serie de reuniones y entrevistas con los usuarios. Esta documentación servirá como entrada para el análisis necesario que se requiere para una comprensión conceptual del sistema.

### Diseño Conceptual

Consiste en formar una descripción concisa de los requerimientos de datos usando un modelo de datos de nivel alto. Esta descripción será independiente de los requerimientos de almacenamiento. Este proceso implica identificar las entidades (y las relaciones entre las entidades) involucradas en el sistema.

### Diseño Físico

Algunos sistemas de base de datos, permiten que el administrador de la base de datos tome decisiones sobre el almacenamiento físico. Se toman generalmente considerando el rendimiento y la disponibilidad de los recursos de hardware.

## Pasos para construir el modelo E-R

1. Identificar las entidades.
2. Eliminar las entidades duplicadas.
3. Enumerar los atributos de cada entidad.
4. Marcar las claves de primarias.
5. Definir las relaciones.
6. Examinar cada tipo de entidad para ver como se relacionan entre sí.
7. Describir la cardinalidad de las relaciones.
8. Eliminar las relaciones redundantes.
