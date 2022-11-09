---
title: "Introducción a las Estructuras de Datos"
date: 2022-10-25T19:49:37-04:00
draft: false
author: "Henrry Bourgeot"
categories: [estructuras de datos, universidad]
tags: [estructuras, universidad, datos]
keywords: [introduccion, estructuras de datos, programacion, universidad]
definition: "En este post encontrarás una introducción a las estructuras de datos"
color: orange
---

Si estás en este post, seguramente estás comenzando a ver lo que son las **estructuras de datos**, por lo que te recomiendo que primero leas este post antes de pasar a otro de la misma [categoría](/categories/estructuras-de-datos).

Primero, debes conocer lo que es un _Dato_ y sus tipos. Para después continuar con el contenido de este post-

## Dato: Concepto y definición

### ¿Qué son?

En el sitio web [TechTarget](techtarget.com/searchdatamanagement/definition/data) lo definen como información que ha sido trasladada en una forma que es más eficiente para mover o procesar. Por lo que podríamos decir que un **dato no es una información**, por lo que es una pieza de información. Se debe tener en cuenta que un dato no es significante, verás el por qué más adelante.

### Tipos

Existen dos tipos de datos, los que son **cualitativos** y otros que son **cuantitativos**. Aquí verás una tabla que tiene la definición y ejemplos de estos:

| Tipos          | Cuantitativos                                                                                                  | Cualitativos                                                                                               |
| -------------- | -------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| **Definición** | Son aquellos que se pueden contar o medir. Expresan con números las propiedades de un objeto, hecho o persona. | No se pueden contar ni medir, expresan de forma nominal las características de un objeto, hecho o persona. |
| **Ejemplos**   | Edad, peso, estatura                                                                                           | Sexo, nombre, descripción de artículos 1                                                                   |

### Operaciones o procesos

Los datos pasan por 5 procesos:

#### a. Captura

Esta operación es la acción de registrar los datos antes de procesar los mismos. La captura puede ser manual (escribirla en el código fuente) o mediante un teclado, lector óptico, ratón, entre otros dispositivos de entrada directa.

#### b. Validación

Es aquel proceso de identificación y corrección de datos durante la captura o incluso después de esta. Tiene el fin de minimizar el número de errores cometidos durante su transcripción. Además, esta operación verifica que los datos que hayan sido capturados cumplan con los parámetros previamente establecidos para lograr un mejor control de los mismos desde el punto de vista de su consistencia.

#### c. Almacenamiento

Esta operación ejecuta un proceso, que guarda los datos capturados y validados para su posterior conservación en cualquier dispositivo físico, como un disco duro, papel, entre otros, inclusive, se podrían almacenar estos en una Base de datos (si no conoces lo que es una, aquí te tengo una [introducción](/introduccion-a-las-bases-de-datos)).

#### d. Recuperación

A través de esta operación se logra acceder posteriormente a los datos almacenados, por ejemplo, imprimir en pantalla los resultados obtenidos de una tabla específica de una base de datos dada.

#### e. Reproducción

Este proceso consiste en trasladar todos los datos de un dispositivo a otro, por ejemplo, de una base de datos a un catálogo de productos con la cantidad disponible de productos.

### Procesamiento

El procesamiento de datos se define como un conjunto de acciones sobre cualquier tipo de dato, para luego poder obtener información oportuna y útil en el logro de un mayor control y mejorar la toma de decisiones. Este procesamiento de datos consta de 4 etapas:

#### Entrada

En esta etapa se realiza el registro de datos en un medio que sea adecuado para su posterior manejo y procesamiento.

#### Proceso

Es la acción de transformar datos en alguna salida que sea esperada, esta transformación consta de 4 pasos:

1. Clasificar: establecer un orden lógico para los datos según un atributo dado.
2. Agrupar: separar sistemáticamente los datos por categorías.
3. Calcular: compuesto por procesos aritméticos y operaciones lógicas para convertir los datos en una forma significativa.
4. Sintetizar: sustituir grandes volúmenes de datos en información sencilla de interpretar.

#### Salida

Es la información procesada que se obtiene del ciclo de procesamiento de datos en un medio de salida, bien sea impreso o electrónico.

#### Evaluación de Resultados

Son analizadas las salidas de acuerdo a los objetivos y metas, de acuerdo a esto se puede ejercer nuevas acciones sobre los datos de entrada de ser necesario.

## Información

Seguro recordarás que dije en la definición que un dato es insignificante, pues esto sucede ya que la información se define como un conjunto de datos que han sido procesados y que además tienen un significado, lo que quiere decir que son relevantes, tienen un propósito y contexto, por lo tanto son útiles para quien necesite tomar decisiones.

Los datos se pueden transformar en información añadiéndoles valor si se realiza lo siguiente:

- Contextualizando: se sabe en qué contexto y para qué propósito se generaron los datos.
- Categorizando: se conoce las unidades de medida que ayudan a interpretarlos.
- Calculando: los datos pueden haber pasado por un proceso previo aplicando matemática o estadística.
- Condensando: los datos se han podido resumir significativa y concisamente.

## Conocimiento

El conocimiento es una mezcla de valores experiencia e información. Es útil para la acción que se origina y aplica en la mente de los conocedores

## Archivos

Es importante saber lo que es en programación un **archivo** , se define como una estructura de datos que recibe memoria secundaria o almacenamiento permanente (discos, discos ópticos, entre otros), además, la forma de clasificación de archivos más básica se realiza de acuerdo al formato que reciben estos.

### Tipos de Archivos

- Binarios: es permanente y está compuesto por registros, y estos a su vez por campos, algo parecido a las tablas de las bases de datos. Se caracterizan por tener un tipo de dato asociado que describe su estructura.
- Texto: es permanente y no está estructurada, pero está formado por una secuencia de caracteres ASCII.

### Tipos de Acceso

Se pueden acceder a los archivos de 4 formas distintas, aunque hay dos tipos que se asemejan mucho.

#### Secuencial

Se accede uno a uno los registros secuencialmente hasta el último o hasta cumplir una condición de búsqueda definida.

#### Random

Se accede en primera instancia la tabla de índices, para así recuperar la dirección de inicio en donde se encuentra el registro buscado.

#### Dinámico

Se accede de igual forma que en el random, solo que se recupera la dirección de inicio **de bloque** donde se encuentra el registro buscado. Este tipo de acceso es permitido o usado en archivos con organización secuencial indexada.

#### Directo

Se utiliza la función de `hashing` para recuperar los registros, aunque sólo se permite para archivos con organización relativa.
